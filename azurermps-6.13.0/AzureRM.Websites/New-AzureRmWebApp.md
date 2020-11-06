---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524204"
---
# <span data-ttu-id="9393b-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="9393b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9393b-102">SYNOPSIS</span></span>
<span data-ttu-id="9393b-103">Azure Web App을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9393b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9393b-104">SYNTAX</span></span>

### <span data-ttu-id="9393b-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9393b-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9393b-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="9393b-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9393b-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="9393b-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9393b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9393b-108">DESCRIPTION</span></span>
<span data-ttu-id="9393b-109">**AzureRmWebApp** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="9393b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9393b-110">EXAMPLES</span></span>

### <span data-ttu-id="9393b-111">예제 1: 웹 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="9393b-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="9393b-112">이 명령은 data center WestUS에서 Default-ContosoSite 이라는 기존 리소스 그룹의 Azure Web App (미국 이름)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="9393b-113">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="9393b-114">변수</span><span class="sxs-lookup"><span data-stu-id="9393b-114">PARAMETERS</span></span>

### <span data-ttu-id="9393b-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9393b-115">-AppServicePlan</span></span>
<span data-ttu-id="9393b-116">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="9393b-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="9393b-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="9393b-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="9393b-118">앱 설정이 HashTable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="9393b-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="9393b-119">-AseName</span></span>
<span data-ttu-id="9393b-120">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="9393b-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="9393b-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9393b-121">-AseResourceGroupName</span></span>
<span data-ttu-id="9393b-122">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9393b-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9393b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9393b-123">-AsJob</span></span>
<span data-ttu-id="9393b-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9393b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9393b-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9393b-125">-ContainerImageName</span></span>
<span data-ttu-id="9393b-126">컨테이너 이미지 이름 및 선택적 태그 (예: Image: tag)</span><span class="sxs-lookup"><span data-stu-id="9393b-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="9393b-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9393b-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9393b-128">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="9393b-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9393b-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9393b-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9393b-130">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="9393b-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9393b-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9393b-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="9393b-132">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="9393b-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9393b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9393b-133">-DefaultProfile</span></span>
<span data-ttu-id="9393b-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393b-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9393b-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9393b-136">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9393b-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9393b-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="9393b-137">-GitRepositoryPath</span></span>
<span data-ttu-id="9393b-138">배포할 웹 응용 프로그램 containign GitHub 리포지토리의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="9393b-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="9393b-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="9393b-140">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="9393b-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="9393b-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="9393b-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="9393b-142">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="9393b-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="9393b-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="9393b-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="9393b-144">원본 Web app 슬롯 포함 옵션</span><span class="sxs-lookup"><span data-stu-id="9393b-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="9393b-145">-위치</span><span class="sxs-lookup"><span data-stu-id="9393b-145">-Location</span></span>
<span data-ttu-id="9393b-146">Location</span><span class="sxs-lookup"><span data-stu-id="9393b-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393b-147">-이름</span><span class="sxs-lookup"><span data-stu-id="9393b-147">-Name</span></span>
<span data-ttu-id="9393b-148">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="9393b-148">WebApp Name</span></span>

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

### <span data-ttu-id="9393b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9393b-149">-ResourceGroupName</span></span>
<span data-ttu-id="9393b-150">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9393b-150">Resource Group Name</span></span>

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

### <span data-ttu-id="9393b-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-151">-SourceWebApp</span></span>
<span data-ttu-id="9393b-152">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="9393b-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="9393b-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9393b-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="9393b-154">기존 traffic manager 프로필의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="9393b-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="9393b-155">-확인</span><span class="sxs-lookup"><span data-stu-id="9393b-155">-Confirm</span></span>
<span data-ttu-id="9393b-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9393b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9393b-157">-WhatIf</span></span>
<span data-ttu-id="9393b-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9393b-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9393b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9393b-160">CommonParameters</span></span>
<span data-ttu-id="9393b-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9393b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9393b-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9393b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9393b-163">입력</span><span class="sxs-lookup"><span data-stu-id="9393b-163">INPUTS</span></span>

### <span data-ttu-id="9393b-164">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="9393b-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="9393b-165">매개 변수: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9393b-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="9393b-166">출력</span><span class="sxs-lookup"><span data-stu-id="9393b-166">OUTPUTS</span></span>

### <span data-ttu-id="9393b-167">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="9393b-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="9393b-168">상속자</span><span class="sxs-lookup"><span data-stu-id="9393b-168">NOTES</span></span>

## <span data-ttu-id="9393b-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9393b-169">RELATED LINKS</span></span>

[<span data-ttu-id="9393b-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="9393b-171">제거-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="9393b-172">다시 시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="9393b-173">시작-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="9393b-174">중지-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9393b-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


