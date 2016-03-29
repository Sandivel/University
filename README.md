# University
Intranet

namespace Mvc3Intranet.Controllers {
    public class HomeController : Controller {
        public ActionResult Index() {
            ViewBag.Message = "Welcome to ASP.NET MVC!";

            return View();
        }

        [Authorize(Users = @"CONTOSO\Rick, CONTOSO\Keith, CONTOSO\Mike")]
        public ActionResult About()
        {
            return View();
        }

        [Authorize(Roles = @"CONTOSO\VBmanagers,CONTOSO\CSmanagers")]
        public ActionResult VB_CS_Managers()
        {
            return View();
        }

        [Authorize(Roles = @"VPs")]
        public ActionResult VP()
        {
            return View();
        }

    }
}
