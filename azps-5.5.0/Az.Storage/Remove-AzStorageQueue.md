---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198412"
---
# <span data-ttu-id="4052c-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4052c-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="4052c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4052c-102">SYNOPSIS</span></span>
<span data-ttu-id="4052c-103">저장소 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-103">Removes a storage queue.</span></span>

## <span data-ttu-id="4052c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4052c-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4052c-105">설명</span><span class="sxs-lookup"><span data-stu-id="4052c-105">DESCRIPTION</span></span>
<span data-ttu-id="4052c-106">**Remove-AzStorageQueue** cmdlet은 저장소 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="4052c-107">예제</span><span class="sxs-lookup"><span data-stu-id="4052c-107">EXAMPLES</span></span>

### <span data-ttu-id="4052c-108">예제 1: 이름으로 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="4052c-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="4052c-109">이 명령은 ContosoQueue01이라는 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="4052c-110">예제 2: 여러 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="4052c-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="4052c-111">이 명령은 Contoso로 시작하는 이름을 사용하여 모든 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="4052c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4052c-112">PARAMETERS</span></span>

### <span data-ttu-id="4052c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4052c-113">-Context</span></span>
<span data-ttu-id="4052c-114">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4052c-115">저장소 컨텍스트를 얻기 위해 New-AzStorageContext cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4052c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4052c-116">-DefaultProfile</span></span>
<span data-ttu-id="4052c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4052c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4052c-118">-Force</span></span>
<span data-ttu-id="4052c-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4052c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4052c-120">-Name</span></span>
<span data-ttu-id="4052c-121">제거할 큐의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="4052c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4052c-122">-PassThru</span></span>
<span data-ttu-id="4052c-123">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4052c-124">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4052c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4052c-125">-Confirm</span></span>
<span data-ttu-id="4052c-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4052c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4052c-127">-WhatIf</span></span>
<span data-ttu-id="4052c-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4052c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4052c-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4052c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4052c-130">CommonParameters</span></span>
<span data-ttu-id="4052c-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4052c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4052c-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4052c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4052c-133">입력</span><span class="sxs-lookup"><span data-stu-id="4052c-133">INPUTS</span></span>

### <span data-ttu-id="4052c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4052c-134">System.String</span></span>

### <span data-ttu-id="4052c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4052c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4052c-136">출력</span><span class="sxs-lookup"><span data-stu-id="4052c-136">OUTPUTS</span></span>

### <span data-ttu-id="4052c-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4052c-137">System.Boolean</span></span>

## <span data-ttu-id="4052c-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4052c-138">NOTES</span></span>

## <span data-ttu-id="4052c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4052c-139">RELATED LINKS</span></span>

[<span data-ttu-id="4052c-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4052c-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="4052c-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4052c-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
