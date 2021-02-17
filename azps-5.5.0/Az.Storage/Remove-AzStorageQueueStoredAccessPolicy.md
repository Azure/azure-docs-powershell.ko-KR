---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198409"
---
# <span data-ttu-id="991cf-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="991cf-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="991cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="991cf-102">SYNOPSIS</span></span>
<span data-ttu-id="991cf-103">Azure 저장소 큐에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="991cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="991cf-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="991cf-105">설명</span><span class="sxs-lookup"><span data-stu-id="991cf-105">DESCRIPTION</span></span>
<span data-ttu-id="991cf-106">**Remove-AzStorageQueueStoredAccessPolicy** cmdlet은 Azure 저장소 큐에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="991cf-107">예제</span><span class="sxs-lookup"><span data-stu-id="991cf-107">EXAMPLES</span></span>

### <span data-ttu-id="991cf-108">예제 1: 저장소 큐에서 저장된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="991cf-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="991cf-109">이 명령은 MyQueue라는 저장소 큐에서 Policy04라는 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="991cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="991cf-110">PARAMETERS</span></span>

### <span data-ttu-id="991cf-111">-Context</span><span class="sxs-lookup"><span data-stu-id="991cf-111">-Context</span></span>
<span data-ttu-id="991cf-112">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="991cf-113">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="991cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="991cf-114">-DefaultProfile</span></span>
<span data-ttu-id="991cf-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="991cf-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="991cf-116">-PassThru</span></span>
<span data-ttu-id="991cf-117">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="991cf-118">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="991cf-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="991cf-119">-Policy</span></span>
<span data-ttu-id="991cf-120">이 cmdlet에서 제거하는 저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="991cf-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="991cf-121">-Queue</span></span>
<span data-ttu-id="991cf-122">Azure 저장소 큐 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="991cf-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="991cf-123">-Confirm</span></span>
<span data-ttu-id="991cf-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="991cf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="991cf-125">-WhatIf</span></span>
<span data-ttu-id="991cf-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="991cf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="991cf-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="991cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="991cf-128">CommonParameters</span></span>
<span data-ttu-id="991cf-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="991cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="991cf-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="991cf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="991cf-131">입력</span><span class="sxs-lookup"><span data-stu-id="991cf-131">INPUTS</span></span>

### <span data-ttu-id="991cf-132">System.String</span><span class="sxs-lookup"><span data-stu-id="991cf-132">System.String</span></span>

### <span data-ttu-id="991cf-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="991cf-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="991cf-134">출력</span><span class="sxs-lookup"><span data-stu-id="991cf-134">OUTPUTS</span></span>

### <span data-ttu-id="991cf-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="991cf-135">System.Boolean</span></span>

## <span data-ttu-id="991cf-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="991cf-136">NOTES</span></span>

## <span data-ttu-id="991cf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="991cf-137">RELATED LINKS</span></span>

[<span data-ttu-id="991cf-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="991cf-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="991cf-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="991cf-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="991cf-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="991cf-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="991cf-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="991cf-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
