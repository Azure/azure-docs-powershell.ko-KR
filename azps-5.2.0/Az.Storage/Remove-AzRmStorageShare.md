---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349394"
---
# <span data-ttu-id="0211a-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0211a-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="0211a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0211a-102">SYNOPSIS</span></span>
<span data-ttu-id="0211a-103">Storage 파일 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="0211a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0211a-104">SYNTAX</span></span>

### <span data-ttu-id="0211a-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0211a-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0211a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0211a-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0211a-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="0211a-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0211a-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="0211a-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0211a-109">설명</span><span class="sxs-lookup"><span data-stu-id="0211a-109">DESCRIPTION</span></span>
<span data-ttu-id="0211a-110">**New-AzRmStorageShare** cmdlet은 Storage 파일 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="0211a-111">예제</span><span class="sxs-lookup"><span data-stu-id="0211a-111">EXAMPLES</span></span>

### <span data-ttu-id="0211a-112">예제 1: Storage 계정 이름 및 공유 이름을 사용하여 Storage 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="0211a-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="0211a-113">이 명령은 Storage 계정 이름 및 공유 이름을 사용하여 Storage 파일 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="0211a-114">예제 2: Storage 계정 개체 및 공유 이름을 사용하여 Storage 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="0211a-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="0211a-115">이 명령은 Storage 계정 개체 및 공유 이름을 사용하여 Storage 파일 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="0211a-116">예제 3: 파이프라인이 있는 Storage 계정의 모든 Storage 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="0211a-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="0211a-117">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage 파일 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="0211a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0211a-118">PARAMETERS</span></span>

### <span data-ttu-id="0211a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0211a-119">-DefaultProfile</span></span>
<span data-ttu-id="0211a-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0211a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0211a-121">-Force</span></span>
<span data-ttu-id="0211a-122">강제로 공유 및 해당 콘텐츠의 모든 콘텐츠를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="0211a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0211a-123">-InputObject</span></span>
<span data-ttu-id="0211a-124">저장소 공유 개체</span><span class="sxs-lookup"><span data-stu-id="0211a-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0211a-125">-Name</span></span>
<span data-ttu-id="0211a-126">공유 이름</span><span class="sxs-lookup"><span data-stu-id="0211a-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0211a-127">-PassThru</span></span>
<span data-ttu-id="0211a-128">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0211a-129">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0211a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0211a-130">-ResourceGroupName</span></span>
<span data-ttu-id="0211a-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0211a-132">-ResourceId</span></span>
<span data-ttu-id="0211a-133">파일 공유 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0211a-134">-StorageAccount</span></span>
<span data-ttu-id="0211a-135">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="0211a-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0211a-136">-StorageAccountName</span></span>
<span data-ttu-id="0211a-137">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0211a-138">-Confirm</span></span>
<span data-ttu-id="0211a-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0211a-140">-WhatIf</span></span>
<span data-ttu-id="0211a-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0211a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0211a-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0211a-143">CommonParameters</span></span>
<span data-ttu-id="0211a-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0211a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0211a-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0211a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0211a-146">입력</span><span class="sxs-lookup"><span data-stu-id="0211a-146">INPUTS</span></span>

### <span data-ttu-id="0211a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0211a-147">System.String</span></span>

### <span data-ttu-id="0211a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0211a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0211a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="0211a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0211a-150">출력</span><span class="sxs-lookup"><span data-stu-id="0211a-150">OUTPUTS</span></span>

### <span data-ttu-id="0211a-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0211a-151">System.Boolean</span></span>

## <span data-ttu-id="0211a-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0211a-152">NOTES</span></span>

## <span data-ttu-id="0211a-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0211a-153">RELATED LINKS</span></span>
