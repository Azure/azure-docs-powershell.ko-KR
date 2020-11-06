---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534779"
---
# <span data-ttu-id="afffd-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="afffd-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="afffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afffd-102">SYNOPSIS</span></span>
<span data-ttu-id="afffd-103">Opts에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 개선 했습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="afffd-104">명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afffd-105">구문과</span><span class="sxs-lookup"><span data-stu-id="afffd-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afffd-106">설명은</span><span class="sxs-lookup"><span data-stu-id="afffd-106">DESCRIPTION</span></span>
<span data-ttu-id="afffd-107">데이터 수집을 통해 Microsoft 클라우드 및 Azure PowerShell을 사용 하는 환경을 개선할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="afffd-108">Azure PowerShell이 동의 하지 않고 데이터를 수집 하지 않음-AzureRmDataCollection를 실행 하 여 명시적으로 옵트인 하거나 cmdlet을 처음 실행할 때 Azure PowerShell에 데이터 수집에 대 한 메시지가 표시 되 면 예를 사용 하 여 사용자에 게 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="afffd-109">Microsoft는 일반적인 문제를 식별 하 고 Azure PowerShell을 사용 하는 환경을 개선 하기 위해 사용 패턴을 식별 하기 위해 수집 된 데이터를 집계 합니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="afffd-110">Microsoft Azure PowerShell은 개인 데이터 또는 개인 식별이 가능한 정보를 수집 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="afffd-111">Disable-AzureRMDataCollection cmdlet을 실행 하 여 현재 사용자의 데이터 수집을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="afffd-112">이렇게 하면 첫 번째 cmdlet이 실행 될 때 현재 사용자에 게 데이터 수집에 대 한 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="afffd-113">현재 사용자에 대해 데이터 수집을 사용 하도록 설정 하려면 Enable-AzureRmDataCollection cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="afffd-114">예제의</span><span class="sxs-lookup"><span data-stu-id="afffd-114">EXAMPLES</span></span>

### <span data-ttu-id="afffd-115">예제 1: 현재 사용자에 대해 데이터 수집을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="afffd-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="afffd-116">이 예제에서는 현재 사용자의 데이터 수집을 사용 하지 않도록 설정 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="afffd-117">변수</span><span class="sxs-lookup"><span data-stu-id="afffd-117">PARAMETERS</span></span>

### <span data-ttu-id="afffd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afffd-118">-DefaultProfile</span></span>
<span data-ttu-id="afffd-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afffd-120">-확인</span><span class="sxs-lookup"><span data-stu-id="afffd-120">-Confirm</span></span>
<span data-ttu-id="afffd-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afffd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afffd-122">-WhatIf</span></span>
<span data-ttu-id="afffd-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afffd-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afffd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afffd-125">CommonParameters</span></span>
<span data-ttu-id="afffd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afffd-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afffd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afffd-128">입력</span><span class="sxs-lookup"><span data-stu-id="afffd-128">INPUTS</span></span>

### <span data-ttu-id="afffd-129">않아야</span><span class="sxs-lookup"><span data-stu-id="afffd-129">None</span></span>
<span data-ttu-id="afffd-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afffd-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="afffd-131">출력</span><span class="sxs-lookup"><span data-stu-id="afffd-131">OUTPUTS</span></span>

### <span data-ttu-id="afffd-132">않아야</span><span class="sxs-lookup"><span data-stu-id="afffd-132">None</span></span>

## <span data-ttu-id="afffd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="afffd-133">NOTES</span></span>

## <span data-ttu-id="afffd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afffd-134">RELATED LINKS</span></span>

[<span data-ttu-id="afffd-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="afffd-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

