---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367074"
---
# <span data-ttu-id="e44fd-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e44fd-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="e44fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e44fd-102">SYNOPSIS</span></span>
<span data-ttu-id="e44fd-103">zipdeploy를 사용하여 ZIP, JAR 또는 WAR 파일에서 Azure 웹앱을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="e44fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="e44fd-104">SYNTAX</span></span>

### <span data-ttu-id="e44fd-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e44fd-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e44fd-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e44fd-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="e44fd-107">설명</span><span class="sxs-lookup"><span data-stu-id="e44fd-107">DESCRIPTION</span></span>
<span data-ttu-id="e44fd-108">**Publish-AzWebApp** cmdlet은 기존 Azure Web App에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="e44fd-109">.NET, Python 또는 Node와 같은 스택을 사용하는 경우 ZIP 파일 또는 WAR 또는 JAR 파일을 사용하는 경우 콘텐츠를 ZIP 파일로 Java.</span><span class="sxs-lookup"><span data-stu-id="e44fd-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="e44fd-110">배포하는 동안 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 즉시 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="e44fd-111">이 cmdlet은 Kudu zipdeploy 및 wardeploy 기능을 사용하여 콘텐츠를 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="e44fd-112">zipdeploy 및 wardeploy가 어떻게 작동하고, 배포를 위해 웹앱을 올바르게 패키지하는 방법에 대한 자세한 내용은 Kudu 위키를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e44fd-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="e44fd-113"> https://aka.ms/kuduzipdeployhttps://aka.ms/kuduwardeployzipdeploy 및 wardeploy에 대한 유용한 세부 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="e44fd-114">예제</span><span class="sxs-lookup"><span data-stu-id="e44fd-114">EXAMPLES</span></span>

### <span data-ttu-id="e44fd-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="e44fd-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="e44fd-116">리소스 그룹의 app.zip Web-WestUS에 속하는 MyApp이라는 웹앱에 웹앱의 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="e44fd-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="e44fd-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="e44fd-118">리소스 그룹 ContosoRG에 속하는 ContosoApp이라는 웹앱의 스테이징 슬롯에 javaproject.war의 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="e44fd-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="e44fd-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="e44fd-120">리소스 그룹 contosoRG에 app.zip ContosoApp이라는 웹앱에 웹앱에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="e44fd-121">cmdlet은 백그라운드 작업에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="e44fd-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="e44fd-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="e44fd-123">예제 5</span><span class="sxs-lookup"><span data-stu-id="e44fd-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="e44fd-124">java_app.jar의 콘텐츠를 리소스 그룹 ContosoRG에 속하는 ContosoApp이라는 웹앱에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="e44fd-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e44fd-125">PARAMETERS</span></span>

### <span data-ttu-id="e44fd-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="e44fd-126">-ArchivePath</span></span>
<span data-ttu-id="e44fd-127">보관 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-127">The path of the archive file.</span></span> <span data-ttu-id="e44fd-128">ZIP, WAR 및 JAR이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-128">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="e44fd-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e44fd-129">-AsJob</span></span>
<span data-ttu-id="e44fd-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e44fd-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e44fd-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e44fd-131">-Force</span></span>
<span data-ttu-id="e44fd-132">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="e44fd-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e44fd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44fd-133">-DefaultProfile</span></span>
<span data-ttu-id="e44fd-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e44fd-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e44fd-135">-Name</span></span>
<span data-ttu-id="e44fd-136">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-136">The name of the web app.</span></span>

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

### <span data-ttu-id="e44fd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44fd-137">-ResourceGroupName</span></span>
<span data-ttu-id="e44fd-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="e44fd-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="e44fd-139">-Slot</span></span>
<span data-ttu-id="e44fd-140">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-140">The name of the web app slot.</span></span>

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

### <span data-ttu-id="e44fd-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e44fd-141">-WebApp</span></span>
<span data-ttu-id="e44fd-142">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="e44fd-142">The web app object</span></span>

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

### <span data-ttu-id="e44fd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44fd-143">CommonParameters</span></span>
<span data-ttu-id="e44fd-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e44fd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44fd-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e44fd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44fd-146">입력</span><span class="sxs-lookup"><span data-stu-id="e44fd-146">INPUTS</span></span>

### <span data-ttu-id="e44fd-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e44fd-147">System.String</span></span>

### <span data-ttu-id="e44fd-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e44fd-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e44fd-149">출력</span><span class="sxs-lookup"><span data-stu-id="e44fd-149">OUTPUTS</span></span>

### <span data-ttu-id="e44fd-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e44fd-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e44fd-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e44fd-151">NOTES</span></span>

## <span data-ttu-id="e44fd-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e44fd-152">RELATED LINKS</span></span>
