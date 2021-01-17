---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491244"
---
# <span data-ttu-id="d88bf-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d88bf-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="d88bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d88bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d88bf-103">Azure Storage 파일 서비스에 대한 서비스 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="d88bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="d88bf-104">SYNTAX</span></span>

### <span data-ttu-id="d88bf-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d88bf-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d88bf-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d88bf-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d88bf-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d88bf-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d88bf-108">설명</span><span class="sxs-lookup"><span data-stu-id="d88bf-108">DESCRIPTION</span></span>
<span data-ttu-id="d88bf-109">**Update-AzStorageFileServiceProperty** cmdlet은 Azure Storage 파일 서비스에 대한 서비스 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="d88bf-110">예제</span><span class="sxs-lookup"><span data-stu-id="d88bf-110">EXAMPLES</span></span>

### <span data-ttu-id="d88bf-111">예제 1: 파일 공유 softdelete 사용</span><span class="sxs-lookup"><span data-stu-id="d88bf-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="d88bf-112">이 명령은 보존 기간이 5일인 파일 공유 softdelete 삭제를 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="d88bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d88bf-113">PARAMETERS</span></span>

### <span data-ttu-id="d88bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88bf-114">-DefaultProfile</span></span>
<span data-ttu-id="d88bf-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d88bf-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d88bf-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="d88bf-117">저장소 계정에 대해 공유 삭제 보존 정책을 사용하도록 설정하고 $true 공유 삭제 보존 정책을 사용하지 않도록 $false.</span><span class="sxs-lookup"><span data-stu-id="d88bf-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="d88bf-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="d88bf-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d88bf-120">-ResourceId</span></span>
<span data-ttu-id="d88bf-121">Storage 계정 리소스 ID 또는 파일 서비스 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d88bf-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="d88bf-122">-ShareRetentionDays</span></span>
<span data-ttu-id="d88bf-123">DeleteRetentionPolicy 공유에 대한 보존 일 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="d88bf-124">이 값은 공유 삭제 보존 정책을 사용하도록 설정하는 경우만 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d88bf-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d88bf-125">-StorageAccount</span></span>
<span data-ttu-id="d88bf-126">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d88bf-126">Storage account object</span></span>

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

### <span data-ttu-id="d88bf-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d88bf-127">-StorageAccountName</span></span>
<span data-ttu-id="d88bf-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="d88bf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d88bf-129">-Confirm</span></span>
<span data-ttu-id="d88bf-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d88bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88bf-131">-WhatIf</span></span>
<span data-ttu-id="d88bf-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d88bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88bf-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d88bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88bf-134">CommonParameters</span></span>
<span data-ttu-id="d88bf-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d88bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88bf-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d88bf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88bf-137">입력</span><span class="sxs-lookup"><span data-stu-id="d88bf-137">INPUTS</span></span>

### <span data-ttu-id="d88bf-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d88bf-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d88bf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d88bf-139">System.String</span></span>

## <span data-ttu-id="d88bf-140">출력</span><span class="sxs-lookup"><span data-stu-id="d88bf-140">OUTPUTS</span></span>

### <span data-ttu-id="d88bf-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d88bf-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="d88bf-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d88bf-142">NOTES</span></span>

## <span data-ttu-id="d88bf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d88bf-143">RELATED LINKS</span></span>
