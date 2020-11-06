---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534719"
---
# <span data-ttu-id="22230-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22230-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="22230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22230-102">SYNOPSIS</span></span>
<span data-ttu-id="22230-103">리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22230-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22230-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22230-104">SYNTAX</span></span>

### <span data-ttu-id="22230-105">GetByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="22230-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22230-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="22230-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22230-107">설명은</span><span class="sxs-lookup"><span data-stu-id="22230-107">DESCRIPTION</span></span>
<span data-ttu-id="22230-108">**AzureRmResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22230-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="22230-109">모든 리소스 그룹을 가져오거나 이름 또는 다른 속성을 기준으로 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22230-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="22230-110">기본적으로이 cmdlet은 현재 구독의 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22230-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="22230-111">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="22230-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="22230-112">예제의</span><span class="sxs-lookup"><span data-stu-id="22230-112">EXAMPLES</span></span>

### <span data-ttu-id="22230-113">예제 1: 이름별로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="22230-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="22230-114">이 명령은 EngineerBlog 이라는 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22230-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="22230-115">예제 2: 리소스 그룹의 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="22230-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="22230-116">이 명령은 ContosoRG 이라는 리소스 그룹을 가져오고 해당 그룹과 연결 된 태그를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="22230-117">예제 3: 위치를 기준으로 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="22230-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="22230-118">예제 4: 특정 위치에 있는 모든 리소스 그룹의 이름 표시</span><span class="sxs-lookup"><span data-stu-id="22230-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="22230-119">예제 5: 이름이 WebServer로 시작 하는 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="22230-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="22230-120">변수</span><span class="sxs-lookup"><span data-stu-id="22230-120">PARAMETERS</span></span>

### <span data-ttu-id="22230-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22230-121">-ApiVersion</span></span>
<span data-ttu-id="22230-122">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="22230-123">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22230-123">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22230-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22230-124">-DefaultProfile</span></span>
<span data-ttu-id="22230-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22230-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22230-126">-Id</span><span class="sxs-lookup"><span data-stu-id="22230-126">-Id</span></span>
<span data-ttu-id="22230-127">가져올 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="22230-128">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22230-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22230-129">-위치</span><span class="sxs-lookup"><span data-stu-id="22230-129">-Location</span></span>
<span data-ttu-id="22230-130">가져올 리소스 그룹의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22230-131">-이름</span><span class="sxs-lookup"><span data-stu-id="22230-131">-Name</span></span>
<span data-ttu-id="22230-132">가져올 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-132">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="22230-133">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22230-133">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22230-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="22230-134">-Pre</span></span>
<span data-ttu-id="22230-135">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="22230-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22230-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22230-136">CommonParameters</span></span>
<span data-ttu-id="22230-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22230-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22230-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22230-139">입력</span><span class="sxs-lookup"><span data-stu-id="22230-139">INPUTS</span></span>

### <span data-ttu-id="22230-140">이름</span><span class="sxs-lookup"><span data-stu-id="22230-140">String</span></span>
<span data-ttu-id="22230-141">속성 이름으로 cmdlet에 입력할 수 있지만 값을 기준으로 하지는 파이프를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22230-141">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="22230-142">출력</span><span class="sxs-lookup"><span data-stu-id="22230-142">OUTPUTS</span></span>

### <span data-ttu-id="22230-143">ResourceManagement PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22230-143">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="22230-144">이 cmdlet은 리소스 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22230-144">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="22230-145">상속자</span><span class="sxs-lookup"><span data-stu-id="22230-145">NOTES</span></span>

## <span data-ttu-id="22230-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22230-146">RELATED LINKS</span></span>

[<span data-ttu-id="22230-147">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22230-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="22230-148">제거-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22230-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="22230-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22230-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


