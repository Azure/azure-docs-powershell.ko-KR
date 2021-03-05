---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961275"
---
# <span data-ttu-id="7f8f4-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f8f4-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="7f8f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8f4-103">Azure 저장소 큐에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="7f8f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f8f4-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f8f4-105">설명</span><span class="sxs-lookup"><span data-stu-id="7f8f4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f8f4-106">**Remove-AzStorageQueueStoredAccessPolicy** cmdlet은 Azure 저장소 큐에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="7f8f4-107">예제</span><span class="sxs-lookup"><span data-stu-id="7f8f4-107">EXAMPLES</span></span>

### <span data-ttu-id="7f8f4-108">예제 1: 저장소 큐에서 저장된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="7f8f4-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="7f8f4-109">이 명령은 MyQueue라는 저장소 큐에서 Policy04라는 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="7f8f4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f8f4-110">PARAMETERS</span></span>

### <span data-ttu-id="7f8f4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7f8f4-111">-Context</span></span>
<span data-ttu-id="7f8f4-112">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7f8f4-113">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7f8f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8f4-114">-DefaultProfile</span></span>
<span data-ttu-id="7f8f4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f8f4-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f8f4-116">-PassThru</span></span>
<span data-ttu-id="7f8f4-117">이 cmdlet은 작업의 성공을 반영하는 **부울을** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7f8f4-118">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7f8f4-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="7f8f4-119">-Policy</span></span>
<span data-ttu-id="7f8f4-120">이 cmdlet이 제거한 저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f8f4-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="7f8f4-121">-Queue</span></span>
<span data-ttu-id="7f8f4-122">Azure Storage 큐 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="7f8f4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="7f8f4-123">-Confirm</span></span>
<span data-ttu-id="7f8f4-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f8f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f8f4-125">-WhatIf</span></span>
<span data-ttu-id="7f8f4-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f8f4-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f8f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8f4-128">CommonParameters</span></span>
<span data-ttu-id="7f8f4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8f4-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7f8f4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8f4-131">입력</span><span class="sxs-lookup"><span data-stu-id="7f8f4-131">INPUTS</span></span>

### <span data-ttu-id="7f8f4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7f8f4-132">System.String</span></span>

### <span data-ttu-id="7f8f4-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7f8f4-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7f8f4-134">출력</span><span class="sxs-lookup"><span data-stu-id="7f8f4-134">OUTPUTS</span></span>

### <span data-ttu-id="7f8f4-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f8f4-135">System.Boolean</span></span>

## <span data-ttu-id="7f8f4-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f8f4-136">NOTES</span></span>

## <span data-ttu-id="7f8f4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f8f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f8f4-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f8f4-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7f8f4-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7f8f4-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7f8f4-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f8f4-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7f8f4-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7f8f4-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
