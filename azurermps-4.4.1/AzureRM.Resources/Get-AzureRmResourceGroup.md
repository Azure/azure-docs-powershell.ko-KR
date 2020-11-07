---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703333"
---
# <span data-ttu-id="2c7ee-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7ee-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="2c7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7ee-103">리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c7ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c7ee-104">SYNTAX</span></span>

### <span data-ttu-id="2c7ee-105">이름에 따라 리소스 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="2c7ee-106">기본값</span><span class="sxs-lookup"><span data-stu-id="2c7ee-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c7ee-107">Id를 기준으로 리소스 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c7ee-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c7ee-108">DESCRIPTION</span></span>
<span data-ttu-id="2c7ee-109">**AzureRmResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="2c7ee-110">모든 리소스 그룹을 가져오거나 이름 또는 다른 속성을 기준으로 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="2c7ee-111">기본적으로이 cmdlet은 현재 구독의 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="2c7ee-112">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="2c7ee-113">예제의</span><span class="sxs-lookup"><span data-stu-id="2c7ee-113">EXAMPLES</span></span>

### <span data-ttu-id="2c7ee-114">예제 1: 이름별로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c7ee-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="2c7ee-115">이 명령은 EngineerBlog 이라는 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="2c7ee-116">예제 2: 리소스 그룹의 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c7ee-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="2c7ee-117">이 명령은 ContosoRG 이라는 리소스 그룹을 가져오고 해당 그룹과 연결 된 태그를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="2c7ee-118">변수</span><span class="sxs-lookup"><span data-stu-id="2c7ee-118">PARAMETERS</span></span>

### <span data-ttu-id="2c7ee-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2c7ee-119">-ApiVersion</span></span>
<span data-ttu-id="2c7ee-120">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2c7ee-121">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2c7ee-122">-Id</span><span class="sxs-lookup"><span data-stu-id="2c7ee-122">-Id</span></span>
<span data-ttu-id="2c7ee-123">가져올 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="2c7ee-124">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ee-125">-위치</span><span class="sxs-lookup"><span data-stu-id="2c7ee-125">-Location</span></span>
<span data-ttu-id="2c7ee-126">가져올 리소스 그룹의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-126">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="2c7ee-127">-이름</span><span class="sxs-lookup"><span data-stu-id="2c7ee-127">-Name</span></span>
<span data-ttu-id="2c7ee-128">가져올 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="2c7ee-129">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c7ee-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="2c7ee-130">-Pre</span></span>
<span data-ttu-id="2c7ee-131">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2c7ee-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ee-132">-DefaultProfile</span></span>
<span data-ttu-id="2c7ee-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c7ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7ee-134">CommonParameters</span></span>
<span data-ttu-id="2c7ee-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7ee-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c7ee-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7ee-137">입력</span><span class="sxs-lookup"><span data-stu-id="2c7ee-137">INPUTS</span></span>

### <span data-ttu-id="2c7ee-138">이름</span><span class="sxs-lookup"><span data-stu-id="2c7ee-138">String</span></span>
<span data-ttu-id="2c7ee-139">속성 이름으로 cmdlet에 입력할 수 있지만 값을 기준으로 하지는 파이프를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2c7ee-140">출력</span><span class="sxs-lookup"><span data-stu-id="2c7ee-140">OUTPUTS</span></span>

### <span data-ttu-id="2c7ee-141">ResourceManagement PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="2c7ee-142">이 cmdlet은 리소스 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c7ee-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="2c7ee-143">상속자</span><span class="sxs-lookup"><span data-stu-id="2c7ee-143">NOTES</span></span>

## <span data-ttu-id="2c7ee-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c7ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c7ee-145">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7ee-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="2c7ee-146">제거-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7ee-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="2c7ee-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7ee-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


