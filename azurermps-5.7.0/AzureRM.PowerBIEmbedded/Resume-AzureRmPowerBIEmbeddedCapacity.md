---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525060"
---
# <span data-ttu-id="d819c-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d819c-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d819c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d819c-102">SYNOPSIS</span></span>
<span data-ttu-id="d819c-103">PowerBI 포함 용량의 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d819c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d819c-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="d819c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d819c-105">DESCRIPTION</span></span>
<span data-ttu-id="d819c-106">Resume-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d819c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d819c-107">EXAMPLES</span></span>

### <span data-ttu-id="d819c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d819c-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="d819c-109">이 명령은 resourcegroup testRG에서 testcapacity 이라는 일시 중지 된 용량을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="d819c-110">변수</span><span class="sxs-lookup"><span data-stu-id="d819c-110">PARAMETERS</span></span>

### <span data-ttu-id="d819c-111">-이름</span><span class="sxs-lookup"><span data-stu-id="d819c-111">-Name</span></span>
<span data-ttu-id="d819c-112">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d819c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d819c-113">-ResourceGroupName</span></span>
<span data-ttu-id="d819c-114">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d819c-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d819c-115">-ResourceId</span></span>
<span data-ttu-id="d819c-116">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d819c-116">Azure resource ID</span></span>

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

### <span data-ttu-id="d819c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d819c-117">-InputObject</span></span>
<span data-ttu-id="d819c-118">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="d819c-118">Input object for Piping</span></span>

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

### <span data-ttu-id="d819c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d819c-119">-Confirm</span></span>
<span data-ttu-id="d819c-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="d819c-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d819c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d819c-121">-WhatIf</span></span>
<span data-ttu-id="d819c-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d819c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d819c-123">CommonParameters</span></span>
<span data-ttu-id="d819c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d819c-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d819c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d819c-126">입력</span><span class="sxs-lookup"><span data-stu-id="d819c-126">INPUTS</span></span>

### <span data-ttu-id="d819c-127">않아야</span><span class="sxs-lookup"><span data-stu-id="d819c-127">None</span></span>
<span data-ttu-id="d819c-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d819c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d819c-129">출력</span><span class="sxs-lookup"><span data-stu-id="d819c-129">OUTPUTS</span></span>

### <span data-ttu-id="d819c-130">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="d819c-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d819c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d819c-131">NOTES</span></span>

## <span data-ttu-id="d819c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d819c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d819c-133">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d819c-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d819c-134">일시 중단-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d819c-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
