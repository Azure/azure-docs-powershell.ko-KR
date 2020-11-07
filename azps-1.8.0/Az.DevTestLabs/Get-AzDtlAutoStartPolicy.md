---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 449206713291499c344975e490c3b0d89ab1d88a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700949"
---
# <span data-ttu-id="20860-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="20860-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="20860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20860-102">SYNOPSIS</span></span>
<span data-ttu-id="20860-103">DevTest Labs의 랩에 대 한 자동 시작 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20860-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="20860-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20860-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20860-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20860-105">DESCRIPTION</span></span>
<span data-ttu-id="20860-106">**AzDtlAutoStartPolicy** cmdlet은 자동 시작을 위해 랩 가상 컴퓨터를 예약 하는 랩의 자동 시작 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20860-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="20860-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 자동 시작에 대 한 랩 가상 컴퓨터의 예약을 허용 하도록 설정한 요일 및 시간을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="20860-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="20860-108">예제의</span><span class="sxs-lookup"><span data-stu-id="20860-108">EXAMPLES</span></span>

## <span data-ttu-id="20860-109">변수</span><span class="sxs-lookup"><span data-stu-id="20860-109">PARAMETERS</span></span>

### <span data-ttu-id="20860-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20860-110">-DefaultProfile</span></span>
<span data-ttu-id="20860-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20860-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20860-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="20860-112">-LabName</span></span>
<span data-ttu-id="20860-113">이 cmdlet이 자동 시작 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20860-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="20860-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20860-114">-ResourceGroupName</span></span>
<span data-ttu-id="20860-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20860-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="20860-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20860-116">CommonParameters</span></span>
<span data-ttu-id="20860-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20860-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20860-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20860-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20860-119">입력</span><span class="sxs-lookup"><span data-stu-id="20860-119">INPUTS</span></span>

### <span data-ttu-id="20860-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20860-120">System.String</span></span>

## <span data-ttu-id="20860-121">출력</span><span class="sxs-lookup"><span data-stu-id="20860-121">OUTPUTS</span></span>

### <span data-ttu-id="20860-122">Microsoft. DevTestLabs. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="20860-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="20860-123">상속자</span><span class="sxs-lookup"><span data-stu-id="20860-123">NOTES</span></span>

## <span data-ttu-id="20860-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20860-124">RELATED LINKS</span></span>

[<span data-ttu-id="20860-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="20860-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


