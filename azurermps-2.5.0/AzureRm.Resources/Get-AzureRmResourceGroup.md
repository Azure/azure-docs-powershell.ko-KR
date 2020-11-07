---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: ede228aef26cf7e4729acf3a6acc0faae3902f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881726"
---
# <span data-ttu-id="9b54e-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b54e-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="9b54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b54e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b54e-103">리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b54e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b54e-104">SYNTAX</span></span>

### <span data-ttu-id="9b54e-105">GetByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b54e-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b54e-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9b54e-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b54e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b54e-107">DESCRIPTION</span></span>
<span data-ttu-id="9b54e-108">**AzureRmResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="9b54e-109">모든 리소스 그룹을 가져오거나 이름 또는 다른 속성을 기준으로 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="9b54e-110">기본적으로이 cmdlet은 현재 구독의 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="9b54e-111">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b54e-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="9b54e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9b54e-112">EXAMPLES</span></span>

### <span data-ttu-id="9b54e-113">예제 1: 이름별로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b54e-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="9b54e-114">이 명령은 EngineerBlog 이라는 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="9b54e-115">예제 2: 리소스 그룹의 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b54e-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="9b54e-116">이 명령은 ContosoRG 이라는 리소스 그룹을 가져오고 해당 그룹과 연결 된 태그를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="9b54e-117">예제 3: 위치를 기준으로 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="9b54e-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="9b54e-118">예제 4: 특정 위치에 있는 모든 리소스 그룹의 이름 표시</span><span class="sxs-lookup"><span data-stu-id="9b54e-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="9b54e-119">예제 5: 이름이 WebServer로 시작 하는 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="9b54e-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="9b54e-120">변수</span><span class="sxs-lookup"><span data-stu-id="9b54e-120">PARAMETERS</span></span>

### <span data-ttu-id="9b54e-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9b54e-121">-ApiVersion</span></span>
<span data-ttu-id="9b54e-122">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9b54e-123">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9b54e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b54e-124">-DefaultProfile</span></span>
<span data-ttu-id="9b54e-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9b54e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b54e-126">-Id</span><span class="sxs-lookup"><span data-stu-id="9b54e-126">-Id</span></span>
<span data-ttu-id="9b54e-127">가져올 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="9b54e-128">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b54e-129">-위치</span><span class="sxs-lookup"><span data-stu-id="9b54e-129">-Location</span></span>
<span data-ttu-id="9b54e-130">가져올 리소스 그룹의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b54e-131">-이름</span><span class="sxs-lookup"><span data-stu-id="9b54e-131">-Name</span></span>
<span data-ttu-id="9b54e-132">가져올 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="9b54e-133">이 매개 변수는 문자열의 시작 및/또는 끝에 있는 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b54e-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="9b54e-134">-Pre</span></span>
<span data-ttu-id="9b54e-135">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9b54e-136">태그</span><span class="sxs-lookup"><span data-stu-id="9b54e-136">-Tag</span></span>
<span data-ttu-id="9b54e-137">리소스 그룹을 필터링 하는 태그 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-137">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b54e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b54e-138">CommonParameters</span></span>
<span data-ttu-id="9b54e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b54e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b54e-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b54e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b54e-141">입력</span><span class="sxs-lookup"><span data-stu-id="9b54e-141">INPUTS</span></span>

### <span data-ttu-id="9b54e-142">않아야</span><span class="sxs-lookup"><span data-stu-id="9b54e-142">None</span></span>

## <span data-ttu-id="9b54e-143">출력</span><span class="sxs-lookup"><span data-stu-id="9b54e-143">OUTPUTS</span></span>

### <span data-ttu-id="9b54e-144">ResourceManagement PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9b54e-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="9b54e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="9b54e-145">NOTES</span></span>

## <span data-ttu-id="9b54e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b54e-146">RELATED LINKS</span></span>

[<span data-ttu-id="9b54e-147">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b54e-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="9b54e-148">제거-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b54e-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="9b54e-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b54e-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


