---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190737"
---
# <span data-ttu-id="3f6a8-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f6a8-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3f6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6a8-103">Azure 저장소 테이블에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="3f6a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f6a8-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f6a8-105">설명</span><span class="sxs-lookup"><span data-stu-id="3f6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="3f6a8-106">**Remove-AzStorageTableStoredAccessPolicy** cmdlet은 Azure 저장소 테이블에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="3f6a8-107">예제</span><span class="sxs-lookup"><span data-stu-id="3f6a8-107">EXAMPLES</span></span>

### <span data-ttu-id="3f6a8-108">예제 1: 저장소 테이블에서 저장된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="3f6a8-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="3f6a8-109">이 명령은 MyTable이라는 저장소 테이블에서 Policy05라는 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="3f6a8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f6a8-110">PARAMETERS</span></span>

### <span data-ttu-id="3f6a8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3f6a8-111">-Context</span></span>
<span data-ttu-id="3f6a8-112">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3f6a8-113">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3f6a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6a8-114">-DefaultProfile</span></span>
<span data-ttu-id="3f6a8-115">Azure와 통신합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-115">communication with Azure.</span></span>

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

### <span data-ttu-id="3f6a8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f6a8-116">-PassThru</span></span>
<span data-ttu-id="3f6a8-117">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3f6a8-118">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3f6a8-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="3f6a8-119">-Policy</span></span>
<span data-ttu-id="3f6a8-120">이 cmdlet에서 제거하는 저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f6a8-121">-Table</span><span class="sxs-lookup"><span data-stu-id="3f6a8-121">-Table</span></span>
<span data-ttu-id="3f6a8-122">Azure 테이블 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="3f6a8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f6a8-123">-Confirm</span></span>
<span data-ttu-id="3f6a8-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f6a8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f6a8-125">-WhatIf</span></span>
<span data-ttu-id="3f6a8-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3f6a8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f6a8-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f6a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6a8-128">CommonParameters</span></span>
<span data-ttu-id="3f6a8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6a8-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3f6a8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6a8-131">입력</span><span class="sxs-lookup"><span data-stu-id="3f6a8-131">INPUTS</span></span>

### <span data-ttu-id="3f6a8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3f6a8-132">System.String</span></span>

### <span data-ttu-id="3f6a8-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f6a8-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3f6a8-134">출력</span><span class="sxs-lookup"><span data-stu-id="3f6a8-134">OUTPUTS</span></span>

### <span data-ttu-id="3f6a8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f6a8-135">System.Boolean</span></span>

## <span data-ttu-id="3f6a8-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f6a8-136">NOTES</span></span>

## <span data-ttu-id="3f6a8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f6a8-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f6a8-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f6a8-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3f6a8-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f6a8-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3f6a8-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f6a8-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3f6a8-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3f6a8-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
