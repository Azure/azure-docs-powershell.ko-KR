---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491331"
---
# <span data-ttu-id="d6cf4-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6cf4-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="d6cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cf4-103">Azure에서 Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d6cf4-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6cf4-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6cf4-105">설명</span><span class="sxs-lookup"><span data-stu-id="d6cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="d6cf4-106">**Remove-AzStorageAccount** cmdlet은 Azure에서 Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="d6cf4-107">예제</span><span class="sxs-lookup"><span data-stu-id="d6cf4-107">EXAMPLES</span></span>

### <span data-ttu-id="d6cf4-108">예제 1: Storage 계정 제거</span><span class="sxs-lookup"><span data-stu-id="d6cf4-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="d6cf4-109">이 명령은 지정된 Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="d6cf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6cf4-110">PARAMETERS</span></span>

### <span data-ttu-id="d6cf4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6cf4-111">-AsJob</span></span>
<span data-ttu-id="d6cf4-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d6cf4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6cf4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cf4-113">-DefaultProfile</span></span>
<span data-ttu-id="d6cf4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cf4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d6cf4-115">-Force</span></span>
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

### <span data-ttu-id="d6cf4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d6cf4-116">-Name</span></span>
<span data-ttu-id="d6cf4-117">제거할 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cf4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6cf4-118">-ResourceGroupName</span></span>
<span data-ttu-id="d6cf4-119">제거할 Storage 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cf4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6cf4-120">-Confirm</span></span>
<span data-ttu-id="d6cf4-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6cf4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6cf4-122">-WhatIf</span></span>
<span data-ttu-id="d6cf4-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d6cf4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6cf4-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6cf4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cf4-125">CommonParameters</span></span>
<span data-ttu-id="d6cf4-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cf4-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d6cf4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cf4-128">입력</span><span class="sxs-lookup"><span data-stu-id="d6cf4-128">INPUTS</span></span>

### <span data-ttu-id="d6cf4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d6cf4-129">System.String</span></span>

## <span data-ttu-id="d6cf4-130">출력</span><span class="sxs-lookup"><span data-stu-id="d6cf4-130">OUTPUTS</span></span>

### <span data-ttu-id="d6cf4-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="d6cf4-131">System.Void</span></span>

## <span data-ttu-id="d6cf4-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6cf4-132">NOTES</span></span>

## <span data-ttu-id="d6cf4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6cf4-133">RELATED LINKS</span></span>

[<span data-ttu-id="d6cf4-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6cf4-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="d6cf4-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6cf4-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="d6cf4-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6cf4-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


