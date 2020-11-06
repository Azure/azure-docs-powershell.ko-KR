---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: de8f9e05cbec17d6a92f3c4e567bd5dce96005ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531655"
---
# <span data-ttu-id="aa482-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="aa482-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="aa482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa482-102">SYNOPSIS</span></span>
<span data-ttu-id="aa482-103">스케줄러 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa482-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa482-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa482-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa482-105">DESCRIPTION</span></span>
<span data-ttu-id="aa482-106">**AzureRmSchedulerJob** Cmdlet은 Azure Scheduler 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="aa482-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa482-107">EXAMPLES</span></span>

## <span data-ttu-id="aa482-108">변수</span><span class="sxs-lookup"><span data-stu-id="aa482-108">PARAMETERS</span></span>

### <span data-ttu-id="aa482-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa482-109">-DefaultProfile</span></span>
<span data-ttu-id="aa482-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa482-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="aa482-111">-JobCollectionName</span></span>
<span data-ttu-id="aa482-112">제거할 작업을 포함 하는 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-112">Specifies the name of a job collection that contains the job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa482-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="aa482-113">-JobName</span></span>
<span data-ttu-id="aa482-114">제거할 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-114">Specifies the name of a job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa482-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa482-115">-PassThru</span></span>
<span data-ttu-id="aa482-116">이 cmdlet이 성공 시 성공 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="aa482-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa482-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa482-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa482-119">제거할 작업의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-119">Specifies the resource group of the job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa482-120">-확인</span><span class="sxs-lookup"><span data-stu-id="aa482-120">-Confirm</span></span>
<span data-ttu-id="aa482-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa482-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa482-122">-WhatIf</span></span>
<span data-ttu-id="aa482-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa482-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa482-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa482-125">CommonParameters</span></span>
<span data-ttu-id="aa482-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa482-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa482-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa482-128">입력</span><span class="sxs-lookup"><span data-stu-id="aa482-128">INPUTS</span></span>

### <span data-ttu-id="aa482-129">않아야</span><span class="sxs-lookup"><span data-stu-id="aa482-129">None</span></span>
<span data-ttu-id="aa482-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa482-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa482-131">출력</span><span class="sxs-lookup"><span data-stu-id="aa482-131">OUTPUTS</span></span>

## <span data-ttu-id="aa482-132">상속자</span><span class="sxs-lookup"><span data-stu-id="aa482-132">NOTES</span></span>

## <span data-ttu-id="aa482-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa482-133">RELATED LINKS</span></span>

[<span data-ttu-id="aa482-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="aa482-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


