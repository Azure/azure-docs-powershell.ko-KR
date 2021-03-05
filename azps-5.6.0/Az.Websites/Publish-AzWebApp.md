---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014459"
---
# <span data-ttu-id="bf047-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bf047-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="bf047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf047-102">SYNOPSIS</span></span>
<span data-ttu-id="bf047-103">zipdeploy를 사용하여 ZIP, JAR 또는 WAR 파일에서 Azure Web App을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="bf047-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf047-104">SYNTAX</span></span>

### <span data-ttu-id="bf047-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="bf047-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf047-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="bf047-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="bf047-107">설명</span><span class="sxs-lookup"><span data-stu-id="bf047-107">DESCRIPTION</span></span>
<span data-ttu-id="bf047-108">**Publish-AzWebApp** cmdlet은 기존 Azure Web App에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="bf047-109">.NET, Python 또는 Node와 같은 스택을 사용하는 경우 ZIP 파일 또는 WAR 또는 JAR 파일을 사용하는 경우 콘텐츠를 ZIP 파일로 Java.</span><span class="sxs-lookup"><span data-stu-id="bf047-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="bf047-110">배포하는 동안 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 바로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="bf047-111">이 cmdlet은 Kudu zipdeploy 및 wardeploy 기능을 사용하여 콘텐츠를 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="bf047-112">zipdeploy 및 wardeploy가 어떻게 작동하고 배포를 위해 웹앱을 올바르게 패키지하는 방법에 대한 자세한 내용은 Kudu wiki를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bf047-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="bf047-113"> https://aka.ms/kuduzipdeploy 및 https://aka.ms/kuduwardeploy zipdeploy 및 wardeploy에 대한 유용한 세부 정보가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="bf047-114">예제</span><span class="sxs-lookup"><span data-stu-id="bf047-114">EXAMPLES</span></span>

### <span data-ttu-id="bf047-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf047-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="bf047-116">리소스 그룹 default-web-WestUS에 app.zip MyApp이라는 웹앱에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="bf047-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="bf047-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="bf047-118">리소스 그룹 ContosoRG에 속하는 ContosoApp이라는 웹앱의 스테이징 슬롯에 javaproject.war의 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="bf047-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="bf047-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="bf047-120">리소스 그룹 contosoRG에 app.zip ContosoApp이라는 웹앱에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="bf047-121">cmdlet은 백그라운드 작업에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="bf047-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="bf047-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="bf047-123">예제 5</span><span class="sxs-lookup"><span data-stu-id="bf047-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="bf047-124">리소스 그룹 ContosoRG에 java_app ContosoApp이라는 웹앱에 java_app.jar의 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="bf047-125">예제 6</span><span class="sxs-lookup"><span data-stu-id="bf047-125">Example 6</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

<span data-ttu-id="bf047-126">리소스 그룹 ContosoRG에 java_app ContosoApp이라는 웹앱에 java_app.jar의 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-126">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="bf047-127">사용자는 요청 시간이 되기 전에 대기하도록 밀리초에서 시간의 시간을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-127">User can Sets the timespan in Milliseconds to wait before the request times out.</span></span>

## <span data-ttu-id="bf047-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf047-128">PARAMETERS</span></span>

### <span data-ttu-id="bf047-129">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="bf047-129">-ArchivePath</span></span>
<span data-ttu-id="bf047-130">보관 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-130">The path of the archive file.</span></span> <span data-ttu-id="bf047-131">ZIP, WAR 및 JAR이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-131">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="bf047-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf047-132">-AsJob</span></span>
<span data-ttu-id="bf047-133">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bf047-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf047-134">-Force</span><span class="sxs-lookup"><span data-stu-id="bf047-134">-Force</span></span>
<span data-ttu-id="bf047-135">강제 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="bf047-135">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="bf047-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf047-136">-DefaultProfile</span></span>
<span data-ttu-id="bf047-137">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf047-138">-Name</span><span class="sxs-lookup"><span data-stu-id="bf047-138">-Name</span></span>
<span data-ttu-id="bf047-139">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-139">The name of the web app.</span></span>

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

### <span data-ttu-id="bf047-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf047-140">-ResourceGroupName</span></span>
<span data-ttu-id="bf047-141">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="bf047-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="bf047-142">-Slot</span></span>
<span data-ttu-id="bf047-143">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-143">The name of the web app slot.</span></span>

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

### <span data-ttu-id="bf047-144">-Timeout</span><span class="sxs-lookup"><span data-stu-id="bf047-144">-Timeout</span></span>
<span data-ttu-id="bf047-145">요청 시간이 되기 전에 기다릴 시간(밀리초)을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-145">Sets the timespan in Milliseconds to wait before the request times out.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf047-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bf047-146">-WebApp</span></span>
<span data-ttu-id="bf047-147">웹앱 개체</span><span class="sxs-lookup"><span data-stu-id="bf047-147">The web app object</span></span>

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

### <span data-ttu-id="bf047-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf047-148">CommonParameters</span></span>
<span data-ttu-id="bf047-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf047-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf047-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bf047-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf047-151">입력</span><span class="sxs-lookup"><span data-stu-id="bf047-151">INPUTS</span></span>

### <span data-ttu-id="bf047-152">System.String</span><span class="sxs-lookup"><span data-stu-id="bf047-152">System.String</span></span>

### <span data-ttu-id="bf047-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="bf047-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bf047-154">출력</span><span class="sxs-lookup"><span data-stu-id="bf047-154">OUTPUTS</span></span>

### <span data-ttu-id="bf047-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="bf047-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bf047-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf047-156">NOTES</span></span>

## <span data-ttu-id="bf047-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf047-157">RELATED LINKS</span></span>
