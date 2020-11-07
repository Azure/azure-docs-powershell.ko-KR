---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700952"
---
# <span data-ttu-id="18fea-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="18fea-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="18fea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fea-102">SYNOPSIS</span></span>
<span data-ttu-id="18fea-103">DevTest 랩에서 랩에서 자동 종료 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18fea-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="18fea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18fea-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18fea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18fea-105">DESCRIPTION</span></span>
<span data-ttu-id="18fea-106">**AzDtlAutoShutdownPolicy** cmdlet은 랩의 자동 종료 정책을 가져와 지정 된 시간에 랩에서 모든 가상 컴퓨터를 자동으로 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="18fea-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="18fea-107">Cmdlet은 정책의 상태를 사용할지 여부와 랩 가상 컴퓨터를 자동으로 종료 하도록 설정한 시간을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fea-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="18fea-108">예제의</span><span class="sxs-lookup"><span data-stu-id="18fea-108">EXAMPLES</span></span>

## <span data-ttu-id="18fea-109">변수</span><span class="sxs-lookup"><span data-stu-id="18fea-109">PARAMETERS</span></span>

### <span data-ttu-id="18fea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fea-110">-DefaultProfile</span></span>
<span data-ttu-id="18fea-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="18fea-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18fea-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="18fea-112">-LabName</span></span>
<span data-ttu-id="18fea-113">이 cmdlet이 자동 종료 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fea-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="18fea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fea-114">-ResourceGroupName</span></span>
<span data-ttu-id="18fea-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fea-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="18fea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fea-116">CommonParameters</span></span>
<span data-ttu-id="18fea-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fea-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fea-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fea-119">입력</span><span class="sxs-lookup"><span data-stu-id="18fea-119">INPUTS</span></span>

### <span data-ttu-id="18fea-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="18fea-120">System.String</span></span>

## <span data-ttu-id="18fea-121">출력</span><span class="sxs-lookup"><span data-stu-id="18fea-121">OUTPUTS</span></span>

### <span data-ttu-id="18fea-122">Microsoft. DevTestLabs. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="18fea-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="18fea-123">상속자</span><span class="sxs-lookup"><span data-stu-id="18fea-123">NOTES</span></span>

## <span data-ttu-id="18fea-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18fea-124">RELATED LINKS</span></span>

[<span data-ttu-id="18fea-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="18fea-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


