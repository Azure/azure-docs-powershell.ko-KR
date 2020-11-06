---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: db2229ed6a0bc5f83dc3d0e856a22b846309ee42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537504"
---
# <span data-ttu-id="bf0ee-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bf0ee-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="bf0ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0ee-103">작업 컬렉션을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf0ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf0ee-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf0ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0ee-106">AzureRmSchedulerJobCollection cmdlet을 **사용** 하면 Azure Scheduler에서 작업을 수집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="bf0ee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf0ee-107">EXAMPLES</span></span>

## <span data-ttu-id="bf0ee-108">변수</span><span class="sxs-lookup"><span data-stu-id="bf0ee-108">PARAMETERS</span></span>

### <span data-ttu-id="bf0ee-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0ee-109">-DefaultProfile</span></span>
<span data-ttu-id="bf0ee-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf0ee-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bf0ee-111">-JobCollectionName</span></span>
<span data-ttu-id="bf0ee-112">작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0ee-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf0ee-113">-PassThru</span></span>
<span data-ttu-id="bf0ee-114">이 cmdlet이 성공 시 성공 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="bf0ee-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf0ee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0ee-116">-ResourceGroupName</span></span>
<span data-ttu-id="bf0ee-117">작업 컬렉션의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0ee-118">-확인</span><span class="sxs-lookup"><span data-stu-id="bf0ee-118">-Confirm</span></span>
<span data-ttu-id="bf0ee-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0ee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf0ee-120">-WhatIf</span></span>
<span data-ttu-id="bf0ee-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf0ee-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0ee-123">CommonParameters</span></span>
<span data-ttu-id="bf0ee-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf0ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0ee-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0ee-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0ee-126">입력</span><span class="sxs-lookup"><span data-stu-id="bf0ee-126">INPUTS</span></span>

### <span data-ttu-id="bf0ee-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf0ee-127">System.String</span></span>

## <span data-ttu-id="bf0ee-128">출력</span><span class="sxs-lookup"><span data-stu-id="bf0ee-128">OUTPUTS</span></span>

### <span data-ttu-id="bf0ee-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf0ee-129">System.String</span></span>

## <span data-ttu-id="bf0ee-130">상속자</span><span class="sxs-lookup"><span data-stu-id="bf0ee-130">NOTES</span></span>

## <span data-ttu-id="bf0ee-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf0ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf0ee-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bf0ee-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bf0ee-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bf0ee-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bf0ee-134">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bf0ee-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bf0ee-135">제거-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bf0ee-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="bf0ee-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="bf0ee-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


