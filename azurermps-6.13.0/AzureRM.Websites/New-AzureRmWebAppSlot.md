---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535024"
---
# <span data-ttu-id="4bbf7-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="4bbf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bbf7-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbf7-103">Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bbf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bbf7-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bbf7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bbf7-105">DESCRIPTION</span></span>
<span data-ttu-id="4bbf7-106">**AzureRmWebAppSlot** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="4bbf7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4bbf7-107">EXAMPLES</span></span>

### <span data-ttu-id="4bbf7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bbf7-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="4bbf7-109">이 명령은 data center ContosoSite에서 Default-WestUS 이라는 기존 리소스 그룹의 기존 웹 앱 이름 아래에 Slot001 라는 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="4bbf7-110">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="4bbf7-111">변수</span><span class="sxs-lookup"><span data-stu-id="4bbf7-111">PARAMETERS</span></span>

### <span data-ttu-id="4bbf7-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4bbf7-112">-AppServicePlan</span></span>
<span data-ttu-id="4bbf7-113">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="4bbf7-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="4bbf7-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="4bbf7-115">앱 설정이 Hashtable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="4bbf7-116">-AseName</span></span>
<span data-ttu-id="4bbf7-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbf7-118">-AseResourceGroupName</span></span>
<span data-ttu-id="4bbf7-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bbf7-120">-AsJob</span></span>
<span data-ttu-id="4bbf7-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4bbf7-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bbf7-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="4bbf7-122">-ContainerImageName</span></span>
<span data-ttu-id="4bbf7-123">컨테이너 이미지 이름 및 선택적 태그 (예: Image: tag)</span><span class="sxs-lookup"><span data-stu-id="4bbf7-123">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="4bbf7-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="4bbf7-125">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="4bbf7-125">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="4bbf7-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="4bbf7-127">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="4bbf7-127">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="4bbf7-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="4bbf7-129">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-129">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbf7-130">-DefaultProfile</span></span>
<span data-ttu-id="4bbf7-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bbf7-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="4bbf7-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="4bbf7-133">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="4bbf7-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="4bbf7-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="4bbf7-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="4bbf7-135">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="4bbf7-135">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="4bbf7-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="4bbf7-137">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="4bbf7-137">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-138">-이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-138">-Name</span></span>
<span data-ttu-id="4bbf7-139">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-139">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbf7-140">-ResourceGroupName</span></span>
<span data-ttu-id="4bbf7-141">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-141">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-142">-슬롯</span><span class="sxs-lookup"><span data-stu-id="4bbf7-142">-Slot</span></span>
<span data-ttu-id="4bbf7-143">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4bbf7-143">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="4bbf7-144">-SourceWebApp</span></span>
<span data-ttu-id="4bbf7-145">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="4bbf7-145">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbf7-146">CommonParameters</span></span>
<span data-ttu-id="4bbf7-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbf7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbf7-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbf7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbf7-149">입력</span><span class="sxs-lookup"><span data-stu-id="4bbf7-149">INPUTS</span></span>

### <span data-ttu-id="4bbf7-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4bbf7-150">System.String</span></span>

### <span data-ttu-id="4bbf7-151">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="4bbf7-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4bbf7-152">매개 변수: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bbf7-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="4bbf7-153">출력</span><span class="sxs-lookup"><span data-stu-id="4bbf7-153">OUTPUTS</span></span>

### <span data-ttu-id="4bbf7-154">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="4bbf7-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="4bbf7-155">상속자</span><span class="sxs-lookup"><span data-stu-id="4bbf7-155">NOTES</span></span>

## <span data-ttu-id="4bbf7-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bbf7-156">RELATED LINKS</span></span>

[<span data-ttu-id="4bbf7-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="4bbf7-158">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="4bbf7-159">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="4bbf7-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="4bbf7-161">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="4bbf7-162">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bbf7-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="4bbf7-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4bbf7-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="4bbf7-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4bbf7-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
