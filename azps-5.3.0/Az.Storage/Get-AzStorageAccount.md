---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376272"
---
# <span data-ttu-id="0f3a1-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f3a1-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="0f3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3a1-103">Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-103">Gets a Storage account.</span></span>

## <span data-ttu-id="0f3a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f3a1-104">SYNTAX</span></span>

### <span data-ttu-id="0f3a1-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f3a1-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f3a1-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f3a1-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f3a1-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f3a1-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f3a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="0f3a1-108">DESCRIPTION</span></span>
<span data-ttu-id="0f3a1-109">**Get-AzStorageAccount** cmdlet은 지정된 Storage 계정 또는 리소스 그룹 또는 구독의 모든 Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="0f3a1-110">예제</span><span class="sxs-lookup"><span data-stu-id="0f3a1-110">EXAMPLES</span></span>

### <span data-ttu-id="0f3a1-111">예제 1: 지정된 Storage 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="0f3a1-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="0f3a1-112">이 명령은 지정된 Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="0f3a1-113">예제 2: 리소스 그룹의 모든 Storage 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="0f3a1-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="0f3a1-114">이 명령은 리소스 그룹의 모든 Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="0f3a1-115">예제 3: 구독의 모든 Storage 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="0f3a1-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="0f3a1-116">이 명령은 구독의 모든 Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="0f3a1-117">예제 4: Blob 복원 상태가 있는 Storage 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="0f3a1-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="0f3a1-118">이 명령은 Blob 복원 상태가 있는 Storage 계정을 얻게 하여 Blob 복원 상태를 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="0f3a1-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="0f3a1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f3a1-119">PARAMETERS</span></span>

### <span data-ttu-id="0f3a1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f3a1-120">-AsJob</span></span>
<span data-ttu-id="0f3a1-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0f3a1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f3a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3a1-122">-DefaultProfile</span></span>
<span data-ttu-id="0f3a1-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f3a1-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="0f3a1-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="0f3a1-125">Storage 계정의 BlobRestoreStatus를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f3a1-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="0f3a1-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="0f3a1-127">Storage 계정의 GeoReplicationStats를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f3a1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0f3a1-128">-Name</span></span>
<span data-ttu-id="0f3a1-129">얻을 Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="0f3a1-131">얻을 Storage 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f3a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3a1-132">CommonParameters</span></span>
<span data-ttu-id="0f3a1-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3a1-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3a1-135">입력</span><span class="sxs-lookup"><span data-stu-id="0f3a1-135">INPUTS</span></span>

### <span data-ttu-id="0f3a1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0f3a1-136">System.String</span></span>

## <span data-ttu-id="0f3a1-137">출력</span><span class="sxs-lookup"><span data-stu-id="0f3a1-137">OUTPUTS</span></span>

### <span data-ttu-id="0f3a1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f3a1-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0f3a1-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f3a1-139">NOTES</span></span>

## <span data-ttu-id="0f3a1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f3a1-140">RELATED LINKS</span></span>

[<span data-ttu-id="0f3a1-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f3a1-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="0f3a1-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f3a1-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="0f3a1-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0f3a1-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


