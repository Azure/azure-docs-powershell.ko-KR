---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212919"
---
# <span data-ttu-id="545cf-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="545cf-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="545cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545cf-102">SYNOPSIS</span></span>
<span data-ttu-id="545cf-103">PowerBI 포함 용량의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="545cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="545cf-104">SYNTAX</span></span>

### <span data-ttu-id="545cf-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="545cf-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545cf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="545cf-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545cf-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="545cf-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545cf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="545cf-108">DESCRIPTION</span></span>
<span data-ttu-id="545cf-109">Remove-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="545cf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="545cf-110">EXAMPLES</span></span>

### <span data-ttu-id="545cf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="545cf-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="545cf-112">이 명령은 resourcegroup testRG에서 testcapacity 이라는 용량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="545cf-113">변수</span><span class="sxs-lookup"><span data-stu-id="545cf-113">PARAMETERS</span></span>

### <span data-ttu-id="545cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545cf-114">-DefaultProfile</span></span>
<span data-ttu-id="545cf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="545cf-116">-InputObject</span></span>
<span data-ttu-id="545cf-117">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="545cf-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="545cf-118">-이름</span><span class="sxs-lookup"><span data-stu-id="545cf-118">-Name</span></span>
<span data-ttu-id="545cf-119">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545cf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="545cf-120">-PassThru</span></span>
<span data-ttu-id="545cf-121">작업이 성공적으로 완료 되 면 삭제 된 용량 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="545cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="545cf-123">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545cf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="545cf-124">-ResourceId</span></span>
<span data-ttu-id="545cf-125">Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="545cf-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="545cf-126">-확인</span><span class="sxs-lookup"><span data-stu-id="545cf-126">-Confirm</span></span>
<span data-ttu-id="545cf-127">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="545cf-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="545cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545cf-128">-WhatIf</span></span>
<span data-ttu-id="545cf-129">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="545cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545cf-130">CommonParameters</span></span>
<span data-ttu-id="545cf-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="545cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545cf-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545cf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545cf-133">입력</span><span class="sxs-lookup"><span data-stu-id="545cf-133">INPUTS</span></span>

### <span data-ttu-id="545cf-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="545cf-134">System.String</span></span>

### <span data-ttu-id="545cf-135">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="545cf-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="545cf-136">출력</span><span class="sxs-lookup"><span data-stu-id="545cf-136">OUTPUTS</span></span>

### <span data-ttu-id="545cf-137">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="545cf-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="545cf-138">상속자</span><span class="sxs-lookup"><span data-stu-id="545cf-138">NOTES</span></span>

## <span data-ttu-id="545cf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="545cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="545cf-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="545cf-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="545cf-141">새로운 AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="545cf-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
