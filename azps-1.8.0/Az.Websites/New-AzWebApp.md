---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 8120b22f02d137ff261b1b4e345b917d6ae82a5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698342"
---
# <span data-ttu-id="ccc3e-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-101">New-AzWebApp</span></span>

## <span data-ttu-id="ccc3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc3e-103">Azure Web App을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="ccc3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccc3e-104">SYNTAX</span></span>

### <span data-ttu-id="ccc3e-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccc3e-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccc3e-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="ccc3e-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccc3e-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccc3e-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccc3e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ccc3e-108">DESCRIPTION</span></span>
<span data-ttu-id="ccc3e-109">**AzWebApp** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="ccc3e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ccc3e-110">EXAMPLES</span></span>

### <span data-ttu-id="ccc3e-111">예제 1: 웹 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="ccc3e-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="ccc3e-112">이 명령은 data center WestUS에서 Default-ContosoSite 이라는 기존 리소스 그룹의 Azure Web App (미국 이름)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="ccc3e-113">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="ccc3e-114">변수</span><span class="sxs-lookup"><span data-stu-id="ccc3e-114">PARAMETERS</span></span>

### <span data-ttu-id="ccc3e-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccc3e-115">-AppServicePlan</span></span>
<span data-ttu-id="ccc3e-116">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="ccc3e-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="ccc3e-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="ccc3e-118">앱 설정이 HashTable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="ccc3e-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="ccc3e-119">-AseName</span></span>
<span data-ttu-id="ccc3e-120">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="ccc3e-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc3e-121">-AseResourceGroupName</span></span>
<span data-ttu-id="ccc3e-122">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="ccc3e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccc3e-123">-AsJob</span></span>
<span data-ttu-id="ccc3e-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ccc3e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccc3e-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ccc3e-125">-ContainerImageName</span></span>
<span data-ttu-id="ccc3e-126">컨테이너 이미지 이름 및 선택적 태그 (예: Image: tag)</span><span class="sxs-lookup"><span data-stu-id="ccc3e-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="ccc3e-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ccc3e-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ccc3e-128">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="ccc3e-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="ccc3e-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ccc3e-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ccc3e-130">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="ccc3e-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="ccc3e-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ccc3e-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="ccc3e-132">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="ccc3e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc3e-133">-DefaultProfile</span></span>
<span data-ttu-id="ccc3e-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccc3e-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ccc3e-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ccc3e-136">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ccc3e-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ccc3e-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="ccc3e-137">-GitRepositoryPath</span></span>
<span data-ttu-id="ccc3e-138">배포할 웹 응용 프로그램이 포함 된 GitHub 리포지토리의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-138">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="ccc3e-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="ccc3e-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="ccc3e-140">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="ccc3e-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="ccc3e-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="ccc3e-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="ccc3e-142">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="ccc3e-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="ccc3e-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ccc3e-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="ccc3e-144">원본 Web app 슬롯 포함 옵션</span><span class="sxs-lookup"><span data-stu-id="ccc3e-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="ccc3e-145">-위치</span><span class="sxs-lookup"><span data-stu-id="ccc3e-145">-Location</span></span>
<span data-ttu-id="ccc3e-146">Location</span><span class="sxs-lookup"><span data-stu-id="ccc3e-146">Location</span></span>

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

### <span data-ttu-id="ccc3e-147">-이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-147">-Name</span></span>
<span data-ttu-id="ccc3e-148">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-148">WebApp Name</span></span>

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

### <span data-ttu-id="ccc3e-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc3e-149">-ResourceGroupName</span></span>
<span data-ttu-id="ccc3e-150">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ccc3e-150">Resource Group Name</span></span>

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

### <span data-ttu-id="ccc3e-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-151">-SourceWebApp</span></span>
<span data-ttu-id="ccc3e-152">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ccc3e-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="ccc3e-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ccc3e-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="ccc3e-154">기존 traffic manager 프로필의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ccc3e-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="ccc3e-155">-확인</span><span class="sxs-lookup"><span data-stu-id="ccc3e-155">-Confirm</span></span>
<span data-ttu-id="ccc3e-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccc3e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccc3e-157">-WhatIf</span></span>
<span data-ttu-id="ccc3e-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccc3e-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccc3e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc3e-160">CommonParameters</span></span>
<span data-ttu-id="ccc3e-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc3e-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc3e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc3e-163">입력</span><span class="sxs-lookup"><span data-stu-id="ccc3e-163">INPUTS</span></span>

### <span data-ttu-id="ccc3e-164">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-164">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ccc3e-165">출력</span><span class="sxs-lookup"><span data-stu-id="ccc3e-165">OUTPUTS</span></span>

### <span data-ttu-id="ccc3e-166">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="ccc3e-166">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ccc3e-167">상속자</span><span class="sxs-lookup"><span data-stu-id="ccc3e-167">NOTES</span></span>

## <span data-ttu-id="ccc3e-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccc3e-168">RELATED LINKS</span></span>

[<span data-ttu-id="ccc3e-169">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-169">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ccc3e-170">제거-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-170">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ccc3e-171">다시 시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-171">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ccc3e-172">시작-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-172">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ccc3e-173">중지-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccc3e-173">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


