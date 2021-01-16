---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349785"
---
# <span data-ttu-id="65d11-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="65d11-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="65d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d11-102">SYNOPSIS</span></span>
<span data-ttu-id="65d11-103">Storage 계정에서 Blob 복원 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="65d11-104">구문</span><span class="sxs-lookup"><span data-stu-id="65d11-104">SYNTAX</span></span>

### <span data-ttu-id="65d11-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="65d11-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65d11-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="65d11-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d11-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="65d11-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d11-108">설명</span><span class="sxs-lookup"><span data-stu-id="65d11-108">DESCRIPTION</span></span>
<span data-ttu-id="65d11-109">**Enable-AzStorageBlobRestorePolicy** cmdlet을 사용하면 Azure Storage Blob 서비스에 대한 Blob 복원 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="65d11-110">예제</span><span class="sxs-lookup"><span data-stu-id="65d11-110">EXAMPLES</span></span>

### <span data-ttu-id="65d11-111">예제 1: Storage 계정에서 Azure Storage Blob service에 대한 Blob 복원 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="65d11-112">이 명령은 먼저 Blob softdelete 및 changefeed를 사용하도록 설정한 다음 Blob 복원 정책을 사용하도록 설정하고 마지막으로 Blob service 속성에서 설정을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="65d11-113">Blob service RestorePolicy.Days는 DeleteRetentionPolicy.Days보다 작아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="65d11-114">Blob softdelete 및 ChangeFeed를 사용하도록 설정해야 Blob 복원 정책을 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="65d11-115">softdelete 및 Changefeed가 방금 사용하도록 설정된 경우 Blob 복원 정책을 사용하도록 설정하기 전에 서버가 설정을 처리할 때까지 잠시 기다려야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="65d11-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65d11-116">PARAMETERS</span></span>

### <span data-ttu-id="65d11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d11-117">-DefaultProfile</span></span>
<span data-ttu-id="65d11-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d11-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65d11-119">-PassThru</span></span>
<span data-ttu-id="65d11-120">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="65d11-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="65d11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d11-121">-ResourceGroupName</span></span>
<span data-ttu-id="65d11-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="65d11-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65d11-123">-ResourceId</span></span>
<span data-ttu-id="65d11-124">Storage 계정 리소스 ID 또는 Blob service 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d11-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="65d11-125">-RestoreDays</span></span>
<span data-ttu-id="65d11-126">Blob을 복원할 수 있는 일 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d11-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="65d11-127">-StorageAccount</span></span>
<span data-ttu-id="65d11-128">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="65d11-128">Storage account object</span></span>

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

### <span data-ttu-id="65d11-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65d11-129">-StorageAccountName</span></span>
<span data-ttu-id="65d11-130">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d11-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65d11-131">-Confirm</span></span>
<span data-ttu-id="65d11-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d11-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d11-133">-WhatIf</span></span>
<span data-ttu-id="65d11-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="65d11-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d11-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d11-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d11-136">CommonParameters</span></span>
<span data-ttu-id="65d11-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65d11-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d11-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="65d11-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d11-139">입력</span><span class="sxs-lookup"><span data-stu-id="65d11-139">INPUTS</span></span>

### <span data-ttu-id="65d11-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="65d11-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="65d11-141">System.String</span><span class="sxs-lookup"><span data-stu-id="65d11-141">System.String</span></span>

## <span data-ttu-id="65d11-142">출력</span><span class="sxs-lookup"><span data-stu-id="65d11-142">OUTPUTS</span></span>

### <span data-ttu-id="65d11-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="65d11-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="65d11-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65d11-144">NOTES</span></span>

## <span data-ttu-id="65d11-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65d11-145">RELATED LINKS</span></span>
