---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: d66203d712de76004d009b98fdc14a18cc69e461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961291"
---
# <span data-ttu-id="a8e38-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8e38-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="a8e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8e38-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e38-103">저장소 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-103">Removes a storage queue.</span></span>

## <span data-ttu-id="a8e38-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8e38-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8e38-105">설명</span><span class="sxs-lookup"><span data-stu-id="a8e38-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e38-106">**Remove-AzStorageQueue** cmdlet은 저장소 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="a8e38-107">예제</span><span class="sxs-lookup"><span data-stu-id="a8e38-107">EXAMPLES</span></span>

### <span data-ttu-id="a8e38-108">예제 1: 이름으로 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="a8e38-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="a8e38-109">이 명령은 ContosoQueue01이라는 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="a8e38-110">예제 2: 여러 저장소 큐 제거</span><span class="sxs-lookup"><span data-stu-id="a8e38-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="a8e38-111">이 명령은 Contoso로 시작하는 이름이 있는 모든 큐를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="a8e38-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a8e38-112">PARAMETERS</span></span>

### <span data-ttu-id="a8e38-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a8e38-113">-Context</span></span>
<span data-ttu-id="a8e38-114">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a8e38-115">저장소 컨텍스트를 얻게 New-AzStorageContext cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a8e38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e38-116">-DefaultProfile</span></span>
<span data-ttu-id="a8e38-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8e38-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a8e38-118">-Force</span></span>
<span data-ttu-id="a8e38-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8e38-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a8e38-120">-Name</span></span>
<span data-ttu-id="a8e38-121">제거할 큐의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="a8e38-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8e38-122">-PassThru</span></span>
<span data-ttu-id="a8e38-123">이 cmdlet은 작업의 성공을 반영하는 **부울을** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a8e38-124">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a8e38-125">-확인</span><span class="sxs-lookup"><span data-stu-id="a8e38-125">-Confirm</span></span>
<span data-ttu-id="a8e38-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e38-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e38-127">-WhatIf</span></span>
<span data-ttu-id="a8e38-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8e38-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e38-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e38-130">CommonParameters</span></span>
<span data-ttu-id="a8e38-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8e38-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e38-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a8e38-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e38-133">입력</span><span class="sxs-lookup"><span data-stu-id="a8e38-133">INPUTS</span></span>

### <span data-ttu-id="a8e38-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a8e38-134">System.String</span></span>

### <span data-ttu-id="a8e38-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8e38-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a8e38-136">출력</span><span class="sxs-lookup"><span data-stu-id="a8e38-136">OUTPUTS</span></span>

### <span data-ttu-id="a8e38-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8e38-137">System.Boolean</span></span>

## <span data-ttu-id="a8e38-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8e38-138">NOTES</span></span>

## <span data-ttu-id="a8e38-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8e38-139">RELATED LINKS</span></span>

[<span data-ttu-id="a8e38-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8e38-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="a8e38-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a8e38-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
