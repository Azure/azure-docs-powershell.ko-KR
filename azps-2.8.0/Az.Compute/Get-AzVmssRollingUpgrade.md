---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssRollingUpgrade.md
ms.openlocfilehash: 344f62f6114eb85e1a9e17b0e4d8c4da0acb93a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697410"
---
# <span data-ttu-id="20cc8-101">Get-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="20cc8-101">Get-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="20cc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="20cc8-103">최신 가상 컴퓨터 배율 집합 롤링 업그레이드의 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-103">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="20cc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20cc8-104">SYNTAX</span></span>

```
Get-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20cc8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="20cc8-106">최신 가상 컴퓨터 배율 집합 롤링 업그레이드의 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-106">Shows the status of the latest virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="20cc8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20cc8-107">EXAMPLES</span></span>

### <span data-ttu-id="20cc8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="20cc8-108">Example 1</span></span>
```
PS C:\> Get-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="20cc8-109">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS001 이라는 VMSS의 최신 롤링 업그레이드 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-109">This command shows  the status of the latest rolling upgrade of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="20cc8-110">변수</span><span class="sxs-lookup"><span data-stu-id="20cc8-110">PARAMETERS</span></span>

### <span data-ttu-id="20cc8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20cc8-111">-DefaultProfile</span></span>
<span data-ttu-id="20cc8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20cc8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20cc8-113">-ResourceGroupName</span></span>
<span data-ttu-id="20cc8-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20cc8-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="20cc8-115">-VMScaleSetName</span></span>
<span data-ttu-id="20cc8-116">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-116">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20cc8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cc8-117">CommonParameters</span></span>
<span data-ttu-id="20cc8-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20cc8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cc8-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20cc8-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cc8-120">입력</span><span class="sxs-lookup"><span data-stu-id="20cc8-120">INPUTS</span></span>

### <span data-ttu-id="20cc8-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20cc8-121">System.String</span></span>

## <span data-ttu-id="20cc8-122">출력</span><span class="sxs-lookup"><span data-stu-id="20cc8-122">OUTPUTS</span></span>

### <span data-ttu-id="20cc8-123">PSRollingUpgradeStatusInfo의. m a.</span><span class="sxs-lookup"><span data-stu-id="20cc8-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSRollingUpgradeStatusInfo</span></span>

## <span data-ttu-id="20cc8-124">상속자</span><span class="sxs-lookup"><span data-stu-id="20cc8-124">NOTES</span></span>

## <span data-ttu-id="20cc8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20cc8-125">RELATED LINKS</span></span>
