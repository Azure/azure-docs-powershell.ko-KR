---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698325"
---
# <span data-ttu-id="02526-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="02526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02526-102">SYNOPSIS</span></span>
<span data-ttu-id="02526-103">Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02526-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="02526-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02526-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02526-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02526-105">DESCRIPTION</span></span>
<span data-ttu-id="02526-106">**AzWebAppSlot** cmdlet은 지정 된 앱 서비스 계획 및 데이터 센터를 사용 하는 지정 된 리소스 그룹에서 Azure 웹 앱 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02526-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="02526-107">예제의</span><span class="sxs-lookup"><span data-stu-id="02526-107">EXAMPLES</span></span>

### <span data-ttu-id="02526-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="02526-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="02526-109">이 명령은 data center ContosoSite에서 Default-WestUS 이라는 기존 리소스 그룹의 기존 웹 앱 이름 아래에 Slot001 라는 슬롯을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02526-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="02526-110">이 명령은 ContosoServicePlan 이라는 기존 App Service 계획을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02526-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="02526-111">변수</span><span class="sxs-lookup"><span data-stu-id="02526-111">PARAMETERS</span></span>

### <span data-ttu-id="02526-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="02526-112">-AppServicePlan</span></span>
<span data-ttu-id="02526-113">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="02526-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="02526-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="02526-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="02526-115">앱 설정이 Hashtable를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="02526-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="02526-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="02526-116">-AseName</span></span>
<span data-ttu-id="02526-117">App Service Environment 이름</span><span class="sxs-lookup"><span data-stu-id="02526-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="02526-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02526-118">-AseResourceGroupName</span></span>
<span data-ttu-id="02526-119">App Service Environment 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="02526-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="02526-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02526-120">-AsJob</span></span>
<span data-ttu-id="02526-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="02526-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02526-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="02526-122">-ContainerImageName</span></span>
<span data-ttu-id="02526-123">컨테이너 이미지 이름 및 선택적 태그 (예: Image: tag)</span><span class="sxs-lookup"><span data-stu-id="02526-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="02526-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="02526-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="02526-125">개인 컨테이너 레지스트리 암호</span><span class="sxs-lookup"><span data-stu-id="02526-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="02526-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="02526-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="02526-127">개인 컨테이너 레지스트리 서버 Url</span><span class="sxs-lookup"><span data-stu-id="02526-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="02526-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="02526-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="02526-129">개인 컨테이너 레지스트리 사용자 이름</span><span class="sxs-lookup"><span data-stu-id="02526-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="02526-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02526-130">-DefaultProfile</span></span>
<span data-ttu-id="02526-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02526-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02526-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="02526-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="02526-133">컨테이너 연속 배포 webhook 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="02526-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="02526-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="02526-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="02526-135">사용자 지정 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="02526-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="02526-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="02526-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="02526-137">원본 컨트롤 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="02526-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="02526-138">-이름</span><span class="sxs-lookup"><span data-stu-id="02526-138">-Name</span></span>
<span data-ttu-id="02526-139">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="02526-139">Webapp Name</span></span>

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

### <span data-ttu-id="02526-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02526-140">-ResourceGroupName</span></span>
<span data-ttu-id="02526-141">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="02526-141">Resource Group Name</span></span>

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

### <span data-ttu-id="02526-142">-슬롯</span><span class="sxs-lookup"><span data-stu-id="02526-142">-Slot</span></span>
<span data-ttu-id="02526-143">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="02526-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="02526-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="02526-144">-SourceWebApp</span></span>
<span data-ttu-id="02526-145">원본 Web app 개체</span><span class="sxs-lookup"><span data-stu-id="02526-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="02526-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02526-146">CommonParameters</span></span>
<span data-ttu-id="02526-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02526-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02526-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02526-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02526-149">입력</span><span class="sxs-lookup"><span data-stu-id="02526-149">INPUTS</span></span>

### <span data-ttu-id="02526-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02526-150">System.String</span></span>

### <span data-ttu-id="02526-151">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="02526-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="02526-152">출력</span><span class="sxs-lookup"><span data-stu-id="02526-152">OUTPUTS</span></span>

### <span data-ttu-id="02526-153">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="02526-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="02526-154">상속자</span><span class="sxs-lookup"><span data-stu-id="02526-154">NOTES</span></span>

## <span data-ttu-id="02526-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02526-155">RELATED LINKS</span></span>

[<span data-ttu-id="02526-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="02526-157">제거-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="02526-158">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="02526-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="02526-160">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="02526-161">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="02526-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="02526-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="02526-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="02526-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="02526-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
