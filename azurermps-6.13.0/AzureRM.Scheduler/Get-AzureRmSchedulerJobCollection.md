---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 402bb79dbd3b767cbc285600b9c81e27f244141e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535600"
---
# <span data-ttu-id="9aec8-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9aec8-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="9aec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aec8-102">SYNOPSIS</span></span>
<span data-ttu-id="9aec8-103">작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aec8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9aec8-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aec8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9aec8-105">DESCRIPTION</span></span>
<span data-ttu-id="9aec8-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler의 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="9aec8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9aec8-107">EXAMPLES</span></span>

## <span data-ttu-id="9aec8-108">변수</span><span class="sxs-lookup"><span data-stu-id="9aec8-108">PARAMETERS</span></span>

### <span data-ttu-id="9aec8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aec8-109">-DefaultProfile</span></span>
<span data-ttu-id="9aec8-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aec8-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9aec8-111">-JobCollectionName</span></span>
<span data-ttu-id="9aec8-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aec8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aec8-113">-ResourceGroupName</span></span>
<span data-ttu-id="9aec8-114">이 cmdlet에서 작업 컬렉션을 가져오는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

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

### <span data-ttu-id="9aec8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aec8-115">CommonParameters</span></span>
<span data-ttu-id="9aec8-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aec8-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aec8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aec8-118">입력</span><span class="sxs-lookup"><span data-stu-id="9aec8-118">INPUTS</span></span>

### <span data-ttu-id="9aec8-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9aec8-119">System.String</span></span>

## <span data-ttu-id="9aec8-120">출력</span><span class="sxs-lookup"><span data-stu-id="9aec8-120">OUTPUTS</span></span>

### <span data-ttu-id="9aec8-121">PSJobCollectionDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="9aec8-121">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="9aec8-122">상속자</span><span class="sxs-lookup"><span data-stu-id="9aec8-122">NOTES</span></span>

## <span data-ttu-id="9aec8-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aec8-123">RELATED LINKS</span></span>

[<span data-ttu-id="9aec8-124">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9aec8-124">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9aec8-125">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9aec8-125">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9aec8-126">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9aec8-126">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9aec8-127">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9aec8-127">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="9aec8-128">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9aec8-128">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


