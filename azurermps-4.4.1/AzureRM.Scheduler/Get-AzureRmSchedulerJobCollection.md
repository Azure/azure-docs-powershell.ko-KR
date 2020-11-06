---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536968"
---
# <span data-ttu-id="87029-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="87029-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="87029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87029-102">SYNOPSIS</span></span>
<span data-ttu-id="87029-103">작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87029-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87029-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87029-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87029-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87029-105">DESCRIPTION</span></span>
<span data-ttu-id="87029-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler의 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87029-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="87029-107">예제의</span><span class="sxs-lookup"><span data-stu-id="87029-107">EXAMPLES</span></span>

## <span data-ttu-id="87029-108">변수</span><span class="sxs-lookup"><span data-stu-id="87029-108">PARAMETERS</span></span>

### <span data-ttu-id="87029-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="87029-109">-JobCollectionName</span></span>
<span data-ttu-id="87029-110">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87029-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="87029-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87029-111">-ResourceGroupName</span></span>
<span data-ttu-id="87029-112">이 cmdlet에서 작업 컬렉션을 가져오는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87029-112">Specifies resource group from which this cmdlet gets job collections.</span></span>

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

### <span data-ttu-id="87029-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87029-113">-DefaultProfile</span></span>
<span data-ttu-id="87029-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87029-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87029-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87029-115">CommonParameters</span></span>
<span data-ttu-id="87029-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87029-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87029-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87029-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87029-118">입력</span><span class="sxs-lookup"><span data-stu-id="87029-118">INPUTS</span></span>

## <span data-ttu-id="87029-119">출력</span><span class="sxs-lookup"><span data-stu-id="87029-119">OUTPUTS</span></span>

### <span data-ttu-id="87029-120">System. 개체</span><span class="sxs-lookup"><span data-stu-id="87029-120">System.Object</span></span>

## <span data-ttu-id="87029-121">상속자</span><span class="sxs-lookup"><span data-stu-id="87029-121">NOTES</span></span>

## <span data-ttu-id="87029-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87029-122">RELATED LINKS</span></span>

[<span data-ttu-id="87029-123">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="87029-123">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="87029-124">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="87029-124">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="87029-125">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="87029-125">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="87029-126">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="87029-126">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="87029-127">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="87029-127">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


