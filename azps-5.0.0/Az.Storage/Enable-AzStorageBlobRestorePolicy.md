---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226493"
---
# <span data-ttu-id="2c327-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="2c327-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="2c327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c327-102">SYNOPSIS</span></span>
<span data-ttu-id="2c327-103">저장소 계정에서 Blob 복원 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="2c327-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c327-104">SYNTAX</span></span>

### <span data-ttu-id="2c327-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c327-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c327-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2c327-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c327-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="2c327-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c327-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c327-108">DESCRIPTION</span></span>
<span data-ttu-id="2c327-109">**AzStorageBlobRestorePolicy** Cmdlet은 Azure Storage blob 서비스에 대해 Blob 복원 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2c327-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2c327-110">EXAMPLES</span></span>

### <span data-ttu-id="2c327-111">예제 1: 저장소 계정에서 Azure Storage Blob 서비스에 대 한 Blob Restore 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2c327-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="2c327-112">이 명령은 먼저 Blob 소프트 삭제 및 changefeed를 사용 하도록 설정 하 고 Blob 복원 정책을 활성화 하 고 마지막으로 Blob service 속성에서 설정을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="2c327-113">Blob 서비스 RestorePolicy 일 수는 DeleteRetentionPolicy 보다 작아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="2c327-114">Blob 소프트 삭제 및 ChangeFeed를 사용 하도록 설정 하기 전에 먼저 blob Restore Policy를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="2c327-115">소프트 삭제 및 Changefeed를 사용 하는 경우 서버에서 설정을 처리 하기 위해 잠시 기다려야 할 수 있습니다. Blob 복원 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="2c327-116">변수</span><span class="sxs-lookup"><span data-stu-id="2c327-116">PARAMETERS</span></span>

### <span data-ttu-id="2c327-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c327-117">-DefaultProfile</span></span>
<span data-ttu-id="2c327-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c327-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c327-119">-PassThru</span></span>
<span data-ttu-id="2c327-120">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="2c327-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="2c327-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c327-121">-ResourceGroupName</span></span>
<span data-ttu-id="2c327-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c327-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c327-123">-ResourceId</span></span>
<span data-ttu-id="2c327-124">저장소 계정 리소스 Id 또는 Blob 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="2c327-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="2c327-125">-RestoreDays</span></span>
<span data-ttu-id="2c327-126">Blob을 복원할 수 있는 일 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="2c327-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c327-127">-StorageAccount</span></span>
<span data-ttu-id="2c327-128">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="2c327-128">Storage account object</span></span>

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

### <span data-ttu-id="2c327-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c327-129">-StorageAccountName</span></span>
<span data-ttu-id="2c327-130">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="2c327-131">-확인</span><span class="sxs-lookup"><span data-stu-id="2c327-131">-Confirm</span></span>
<span data-ttu-id="2c327-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c327-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c327-133">-WhatIf</span></span>
<span data-ttu-id="2c327-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c327-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c327-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c327-136">CommonParameters</span></span>
<span data-ttu-id="2c327-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c327-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c327-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c327-139">입력</span><span class="sxs-lookup"><span data-stu-id="2c327-139">INPUTS</span></span>

### <span data-ttu-id="2c327-140">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c327-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2c327-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c327-141">System.String</span></span>

## <span data-ttu-id="2c327-142">출력</span><span class="sxs-lookup"><span data-stu-id="2c327-142">OUTPUTS</span></span>

### <span data-ttu-id="2c327-143">PSRestorePolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c327-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="2c327-144">상속자</span><span class="sxs-lookup"><span data-stu-id="2c327-144">NOTES</span></span>

## <span data-ttu-id="2c327-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c327-145">RELATED LINKS</span></span>
