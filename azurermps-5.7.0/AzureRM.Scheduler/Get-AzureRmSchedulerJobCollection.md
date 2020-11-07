---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703995"
---
# <span data-ttu-id="f5e5e-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5e5e-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="f5e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e5e-103">작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5e5e-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5e5e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="f5e5e-106">**AzureRmSchedulerJobCollection** Cmdlet은 Azure Scheduler의 작업 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="f5e5e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5e5e-107">EXAMPLES</span></span>

## <span data-ttu-id="f5e5e-108">변수</span><span class="sxs-lookup"><span data-stu-id="f5e5e-108">PARAMETERS</span></span>

### <span data-ttu-id="f5e5e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e5e-109">-DefaultProfile</span></span>
<span data-ttu-id="f5e5e-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5e5e-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f5e5e-111">-JobCollectionName</span></span>
<span data-ttu-id="f5e5e-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e5e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e5e-113">-ResourceGroupName</span></span>
<span data-ttu-id="f5e5e-114">이 cmdlet에서 작업 컬렉션을 가져오는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e5e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e5e-115">CommonParameters</span></span>
<span data-ttu-id="f5e5e-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e5e-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e5e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e5e-118">입력</span><span class="sxs-lookup"><span data-stu-id="f5e5e-118">INPUTS</span></span>

### <span data-ttu-id="f5e5e-119">않아야</span><span class="sxs-lookup"><span data-stu-id="f5e5e-119">None</span></span>
<span data-ttu-id="f5e5e-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5e5e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5e5e-121">출력</span><span class="sxs-lookup"><span data-stu-id="f5e5e-121">OUTPUTS</span></span>

### <span data-ttu-id="f5e5e-122">System. 개체</span><span class="sxs-lookup"><span data-stu-id="f5e5e-122">System.Object</span></span>

## <span data-ttu-id="f5e5e-123">상속자</span><span class="sxs-lookup"><span data-stu-id="f5e5e-123">NOTES</span></span>

## <span data-ttu-id="f5e5e-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5e5e-124">RELATED LINKS</span></span>

[<span data-ttu-id="f5e5e-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5e5e-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f5e5e-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5e5e-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f5e5e-127">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5e5e-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f5e5e-128">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5e5e-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f5e5e-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f5e5e-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


