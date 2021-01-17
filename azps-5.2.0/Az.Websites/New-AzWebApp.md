---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324015"
---
# <span data-ttu-id="dd37e-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-101">New-AzWebApp</span></span>

## <span data-ttu-id="dd37e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd37e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd37e-103">Azure 웹앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="dd37e-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd37e-104">SYNTAX</span></span>

### <span data-ttu-id="dd37e-105">SimpleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dd37e-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd37e-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="dd37e-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd37e-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd37e-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd37e-108">설명</span><span class="sxs-lookup"><span data-stu-id="dd37e-108">DESCRIPTION</span></span>
<span data-ttu-id="dd37e-109">**New-AzWebApp** cmdlet은 지정된 App Service 계획 및 데이터 센터를 사용하는 지정된 리소스 그룹에 Azure 웹앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="dd37e-110">예제</span><span class="sxs-lookup"><span data-stu-id="dd37e-110">EXAMPLES</span></span>

### <span data-ttu-id="dd37e-111">예제 1: 웹앱 만들기</span><span class="sxs-lookup"><span data-stu-id="dd37e-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="dd37e-112">이 명령은 미국 서부 데이터 센터의 Default-Web-WestUS라는 기존 리소스 그룹에 ContosoSite라는 Azure 웹앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="dd37e-113">이 명령은 ContosoServicePlan이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="dd37e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd37e-114">PARAMETERS</span></span>

### <span data-ttu-id="dd37e-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dd37e-115">-AppServicePlan</span></span>
<span data-ttu-id="dd37e-116">App Service 계획 이름 또는 App Service 계획 ID입니다. WebApp 및 App Service 계획이 다른 리소스 그룹에 있는 경우 이름 대신 ID를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="dd37e-117">App Service 계획 ID는 $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id App Service 계획 ID를 반환하여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="dd37e-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="dd37e-119">앱 설정이 해시테이블을 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="dd37e-120">-AseName</span></span>
<span data-ttu-id="dd37e-121">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="dd37e-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd37e-122">-AseResourceGroupName</span></span>
<span data-ttu-id="dd37e-123">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dd37e-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd37e-124">-AsJob</span></span>
<span data-ttu-id="dd37e-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dd37e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd37e-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="dd37e-126">-ContainerImageName</span></span>
<span data-ttu-id="dd37e-127">컨테이너 이미지 이름 및 선택적 태그(예: image:tag)</span><span class="sxs-lookup"><span data-stu-id="dd37e-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="dd37e-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="dd37e-129">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="dd37e-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="dd37e-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="dd37e-131">개인 컨테이너 레지스트리 서버 URL</span><span class="sxs-lookup"><span data-stu-id="dd37e-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="dd37e-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="dd37e-133">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="dd37e-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd37e-134">-DefaultProfile</span></span>
<span data-ttu-id="dd37e-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd37e-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="dd37e-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="dd37e-137">컨테이너 연속 배포 웹후크를 활성화/비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="dd37e-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="dd37e-138">-GitRepositoryPath</span></span>
<span data-ttu-id="dd37e-139">배포할 웹 애플리케이션을 포함하는 GitHub 리포지토리의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="dd37e-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="dd37e-141">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="dd37e-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="dd37e-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="dd37e-143">소스 제어 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="dd37e-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="dd37e-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="dd37e-145">원본 WebApp 슬롯 포함 옵션</span><span class="sxs-lookup"><span data-stu-id="dd37e-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-146">-Location</span><span class="sxs-lookup"><span data-stu-id="dd37e-146">-Location</span></span>
<span data-ttu-id="dd37e-147">위치</span><span class="sxs-lookup"><span data-stu-id="dd37e-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-148">-Name</span><span class="sxs-lookup"><span data-stu-id="dd37e-148">-Name</span></span>
<span data-ttu-id="dd37e-149">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="dd37e-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd37e-150">-ResourceGroupName</span></span>
<span data-ttu-id="dd37e-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dd37e-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-152">-SourceWebApp</span></span>
<span data-ttu-id="dd37e-153">원본 WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="dd37e-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dd37e-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="dd37e-155">기존 Traffic Manager 프로필의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="dd37e-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd37e-156">-Confirm</span></span>
<span data-ttu-id="dd37e-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd37e-158">-WhatIf</span></span>
<span data-ttu-id="dd37e-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dd37e-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd37e-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd37e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd37e-161">CommonParameters</span></span>
<span data-ttu-id="dd37e-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd37e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd37e-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dd37e-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd37e-164">입력</span><span class="sxs-lookup"><span data-stu-id="dd37e-164">INPUTS</span></span>

### <span data-ttu-id="dd37e-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="dd37e-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dd37e-166">출력</span><span class="sxs-lookup"><span data-stu-id="dd37e-166">OUTPUTS</span></span>

### <span data-ttu-id="dd37e-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="dd37e-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dd37e-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd37e-168">NOTES</span></span>

## <span data-ttu-id="dd37e-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd37e-169">RELATED LINKS</span></span>

[<span data-ttu-id="dd37e-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="dd37e-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="dd37e-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="dd37e-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="dd37e-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dd37e-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


