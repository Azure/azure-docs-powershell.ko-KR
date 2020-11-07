---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698324"
---
# <span data-ttu-id="31b8c-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="31b8c-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="31b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="31b8c-103">Zipdeploy를 사용 하 여 ZIP, JAR 또는 WAR 파일에서 Azure 웹 앱을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="31b8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31b8c-104">SYNTAX</span></span>

### <span data-ttu-id="31b8c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="31b8c-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b8c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="31b8c-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31b8c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="31b8c-107">DESCRIPTION</span></span>
<span data-ttu-id="31b8c-108">**AzWebApp** cmdlet은 콘텐츠를 기존 Azure Web App에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="31b8c-109">.NET, Python 또는 Node와 같은 스택을 사용 하거나, Java를 사용 하는 경우 WAR 또는 JAR 파일의 경우 콘텐츠는 ZIP 파일에 패키지 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="31b8c-110">배포 중에 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 실행할 준비가 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="31b8c-111">이 cmdlet은 Kudu zipdeploy 및 워 하는 배포 기능을 사용 하 여 콘텐츠를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="31b8c-112">Zipdeploy 및 Kudu에서 작업을 배포 하는 방법과 배포를 위해 웹 앱을 올바르게 패키지 하는 방법에 대 한 자세한 내용은 wiki를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31b8c-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="31b8c-113"> https://aka.ms/kuduzipdeployhttps://aka.ms/kuduwardeployzipdeploy 및 워 배포에 대 한 유용한 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="31b8c-114">예제의</span><span class="sxs-lookup"><span data-stu-id="31b8c-114">EXAMPLES</span></span>

### <span data-ttu-id="31b8c-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="31b8c-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="31b8c-116">리소스 그룹 Default-WestUS에 속하는 MyApp 라는 웹 앱에 app.zip의 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="31b8c-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="31b8c-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="31b8c-118">리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱의 스테이징 슬롯에 javaproject의 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="31b8c-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="31b8c-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="31b8c-120">app.zip의 콘텐츠를 리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="31b8c-121">Cmdlet은 백그라운드 작업에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="31b8c-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="31b8c-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="31b8c-123">리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱에 .jar java_app의 콘텐츠를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="31b8c-124">변수</span><span class="sxs-lookup"><span data-stu-id="31b8c-124">PARAMETERS</span></span>

### <span data-ttu-id="31b8c-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="31b8c-125">-ArchivePath</span></span>
<span data-ttu-id="31b8c-126">보관 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-126">The path of the archive file.</span></span> <span data-ttu-id="31b8c-127">ZIP, 전쟁, JAR를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-127">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31b8c-128">-AsJob</span></span>
<span data-ttu-id="31b8c-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="31b8c-129">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b8c-130">-DefaultProfile</span></span>
<span data-ttu-id="31b8c-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-132">-이름</span><span class="sxs-lookup"><span data-stu-id="31b8c-132">-Name</span></span>
<span data-ttu-id="31b8c-133">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-133">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b8c-134">-ResourceGroupName</span></span>
<span data-ttu-id="31b8c-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-136">-슬롯</span><span class="sxs-lookup"><span data-stu-id="31b8c-136">-Slot</span></span>
<span data-ttu-id="31b8c-137">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-137">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-138">-Web app</span><span class="sxs-lookup"><span data-stu-id="31b8c-138">-WebApp</span></span>
<span data-ttu-id="31b8c-139">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="31b8c-139">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b8c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b8c-140">CommonParameters</span></span>
<span data-ttu-id="31b8c-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b8c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b8c-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b8c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b8c-143">입력</span><span class="sxs-lookup"><span data-stu-id="31b8c-143">INPUTS</span></span>

### <span data-ttu-id="31b8c-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31b8c-144">System.String</span></span>

### <span data-ttu-id="31b8c-145">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="31b8c-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="31b8c-146">출력</span><span class="sxs-lookup"><span data-stu-id="31b8c-146">OUTPUTS</span></span>

### <span data-ttu-id="31b8c-147">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="31b8c-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="31b8c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="31b8c-148">NOTES</span></span>

## <span data-ttu-id="31b8c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31b8c-149">RELATED LINKS</span></span>
