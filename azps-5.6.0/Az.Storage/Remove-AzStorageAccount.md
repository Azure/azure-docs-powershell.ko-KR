---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: b3487cd3a54b2537a8cfd0b4f34e5c962175f1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002299"
---
# <span data-ttu-id="663f9-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663f9-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="663f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="663f9-102">SYNOPSIS</span></span>
<span data-ttu-id="663f9-103">Azure에서 Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="663f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="663f9-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="663f9-105">설명</span><span class="sxs-lookup"><span data-stu-id="663f9-105">DESCRIPTION</span></span>
<span data-ttu-id="663f9-106">**Remove-AzStorageAccount** cmdlet은 Azure에서 Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="663f9-107">예제</span><span class="sxs-lookup"><span data-stu-id="663f9-107">EXAMPLES</span></span>

### <span data-ttu-id="663f9-108">예제 1: Storage 계정 제거</span><span class="sxs-lookup"><span data-stu-id="663f9-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="663f9-109">이 명령은 지정된 Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="663f9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="663f9-110">PARAMETERS</span></span>

### <span data-ttu-id="663f9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="663f9-111">-AsJob</span></span>
<span data-ttu-id="663f9-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="663f9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="663f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663f9-113">-DefaultProfile</span></span>
<span data-ttu-id="663f9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663f9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="663f9-115">-Force</span></span>
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

### <span data-ttu-id="663f9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="663f9-116">-Name</span></span>
<span data-ttu-id="663f9-117">제거할 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="663f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="663f9-119">제거할 Storage 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="663f9-120">-확인</span><span class="sxs-lookup"><span data-stu-id="663f9-120">-Confirm</span></span>
<span data-ttu-id="663f9-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="663f9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="663f9-122">-WhatIf</span></span>
<span data-ttu-id="663f9-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="663f9-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="663f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663f9-125">CommonParameters</span></span>
<span data-ttu-id="663f9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="663f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663f9-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="663f9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663f9-128">입력</span><span class="sxs-lookup"><span data-stu-id="663f9-128">INPUTS</span></span>

### <span data-ttu-id="663f9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="663f9-129">System.String</span></span>

## <span data-ttu-id="663f9-130">출력</span><span class="sxs-lookup"><span data-stu-id="663f9-130">OUTPUTS</span></span>

### <span data-ttu-id="663f9-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="663f9-131">System.Void</span></span>

## <span data-ttu-id="663f9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="663f9-132">NOTES</span></span>

## <span data-ttu-id="663f9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="663f9-133">RELATED LINKS</span></span>

[<span data-ttu-id="663f9-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663f9-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="663f9-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663f9-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="663f9-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663f9-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


