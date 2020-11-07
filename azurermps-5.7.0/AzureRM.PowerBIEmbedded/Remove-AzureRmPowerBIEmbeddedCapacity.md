---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703254"
---
# <span data-ttu-id="f9d9d-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f9d9d-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f9d9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d9d-103">PowerBI 포함 용량의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9d9d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9d9d-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="f9d9d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f9d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="f9d9d-106">Remove-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f9d9d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f9d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="f9d9d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9d9d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="f9d9d-109">이 명령은 resourcegroup testRG에서 testcapacity 이라는 용량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="f9d9d-110">변수</span><span class="sxs-lookup"><span data-stu-id="f9d9d-110">PARAMETERS</span></span>

### <span data-ttu-id="f9d9d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d9d-111">-ResourceGroupName</span></span>
<span data-ttu-id="f9d9d-112">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="f9d9d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="f9d9d-113">-Name</span></span>
<span data-ttu-id="f9d9d-114">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="f9d9d-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d9d-115">-ResourceId</span></span>
<span data-ttu-id="f9d9d-116">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f9d9d-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d9d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d9d-117">-InputObject</span></span>
<span data-ttu-id="f9d9d-118">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="f9d9d-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d9d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9d9d-119">-PassThru</span></span>
<span data-ttu-id="f9d9d-120">작업이 성공적으로 완료 되 면 삭제 된 용량 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-120">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f9d9d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f9d9d-121">-Confirm</span></span>
<span data-ttu-id="f9d9d-122">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="f9d9d-122">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d9d-123">-WhatIf</span></span>
<span data-ttu-id="f9d9d-124">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-124">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d9d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d9d-125">CommonParameters</span></span>
<span data-ttu-id="f9d9d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d9d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9d9d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d9d-128">입력</span><span class="sxs-lookup"><span data-stu-id="f9d9d-128">INPUTS</span></span>

### <span data-ttu-id="f9d9d-129">않아야</span><span class="sxs-lookup"><span data-stu-id="f9d9d-129">None</span></span>
<span data-ttu-id="f9d9d-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d9d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9d9d-131">출력</span><span class="sxs-lookup"><span data-stu-id="f9d9d-131">OUTPUTS</span></span>

### <span data-ttu-id="f9d9d-132">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="f9d9d-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f9d9d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f9d9d-133">NOTES</span></span>

## <span data-ttu-id="f9d9d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9d9d-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9d9d-135">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f9d9d-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f9d9d-136">새로운 AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f9d9d-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
