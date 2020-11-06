---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: 544d019547616ab7fc37804e150115eacc8a0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526431"
---
# <span data-ttu-id="2d1c7-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d1c7-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="2d1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1c7-103">저장소 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d1c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d1c7-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d1c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d1c7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d1c7-106">**AzureStorageQueue** cmdlet은 저장소 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="2d1c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2d1c7-107">EXAMPLES</span></span>

### <span data-ttu-id="2d1c7-108">예제 1: 이름으로 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="2d1c7-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="2d1c7-109">이 명령은 ContosoQueue01 이라는 대기열을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="2d1c7-110">예제 2: 여러 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="2d1c7-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="2d1c7-111">이 명령은 Contoso로 시작 하는 이름의 모든 큐를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="2d1c7-112">변수</span><span class="sxs-lookup"><span data-stu-id="2d1c7-112">PARAMETERS</span></span>

### <span data-ttu-id="2d1c7-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2d1c7-113">-Context</span></span>
<span data-ttu-id="2d1c7-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2d1c7-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d1c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1c7-116">-DefaultProfile</span></span>
<span data-ttu-id="2d1c7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d1c7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2d1c7-118">-Force</span></span>
<span data-ttu-id="2d1c7-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d1c7-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2d1c7-120">-Name</span></span>
<span data-ttu-id="2d1c7-121">제거할 대기열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d1c7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d1c7-122">-PassThru</span></span>
<span data-ttu-id="2d1c7-123">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2d1c7-124">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2d1c7-125">-확인</span><span class="sxs-lookup"><span data-stu-id="2d1c7-125">-Confirm</span></span>
<span data-ttu-id="2d1c7-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d1c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d1c7-127">-WhatIf</span></span>
<span data-ttu-id="2d1c7-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d1c7-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d1c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1c7-130">CommonParameters</span></span>
<span data-ttu-id="2d1c7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d1c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1c7-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d1c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1c7-133">입력</span><span class="sxs-lookup"><span data-stu-id="2d1c7-133">INPUTS</span></span>

### <span data-ttu-id="2d1c7-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d1c7-134">System.String</span></span>

### <span data-ttu-id="2d1c7-135">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d1c7-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d1c7-136">출력</span><span class="sxs-lookup"><span data-stu-id="2d1c7-136">OUTPUTS</span></span>

### <span data-ttu-id="2d1c7-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2d1c7-137">System.Boolean</span></span>

## <span data-ttu-id="2d1c7-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2d1c7-138">NOTES</span></span>

## <span data-ttu-id="2d1c7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d1c7-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d1c7-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d1c7-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="2d1c7-141">새로운 AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2d1c7-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)