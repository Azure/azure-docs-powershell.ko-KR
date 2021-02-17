---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207824"
---
# <span data-ttu-id="43468-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="43468-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="43468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43468-102">SYNOPSIS</span></span>
<span data-ttu-id="43468-103">Azure Storage Blob Service에 대한 삭제 보존 정책을 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="43468-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="43468-104">구문</span><span class="sxs-lookup"><span data-stu-id="43468-104">SYNTAX</span></span>

### <span data-ttu-id="43468-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="43468-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43468-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="43468-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43468-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="43468-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43468-108">설명</span><span class="sxs-lookup"><span data-stu-id="43468-108">DESCRIPTION</span></span>
<span data-ttu-id="43468-109">**Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet을 사용하면 Azure Storage Blob service에 대한 삭제 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43468-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="43468-110">예제</span><span class="sxs-lookup"><span data-stu-id="43468-110">EXAMPLES</span></span>

### <span data-ttu-id="43468-111">예제 1: Blob service에 대한 삭제 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="43468-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="43468-112">이 명령은 Blob service에 대한 삭제 보존 정책을 설정하고 삭제된 Blob 보존 기간을 4로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="43468-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="43468-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43468-113">PARAMETERS</span></span>

### <span data-ttu-id="43468-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43468-114">-DefaultProfile</span></span>
<span data-ttu-id="43468-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43468-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43468-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43468-116">-PassThru</span></span>
<span data-ttu-id="43468-117">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="43468-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="43468-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43468-118">-ResourceGroupName</span></span>
<span data-ttu-id="43468-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43468-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="43468-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43468-120">-ResourceId</span></span>
<span data-ttu-id="43468-121">Storage 계정 리소스 ID 또는 Blob service 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="43468-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="43468-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="43468-122">-RetentionDays</span></span>
<span data-ttu-id="43468-123">DeleteRetentionPolicy에 대한 보존 일 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="43468-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="43468-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="43468-124">-StorageAccount</span></span>
<span data-ttu-id="43468-125">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="43468-125">Storage account object</span></span>

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

### <span data-ttu-id="43468-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="43468-126">-StorageAccountName</span></span>
<span data-ttu-id="43468-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43468-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="43468-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43468-128">-Confirm</span></span>
<span data-ttu-id="43468-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43468-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43468-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43468-130">-WhatIf</span></span>
<span data-ttu-id="43468-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="43468-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43468-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43468-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43468-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43468-133">CommonParameters</span></span>
<span data-ttu-id="43468-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43468-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43468-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="43468-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43468-136">입력</span><span class="sxs-lookup"><span data-stu-id="43468-136">INPUTS</span></span>

### <span data-ttu-id="43468-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43468-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="43468-138">System.String</span><span class="sxs-lookup"><span data-stu-id="43468-138">System.String</span></span>

## <span data-ttu-id="43468-139">출력</span><span class="sxs-lookup"><span data-stu-id="43468-139">OUTPUTS</span></span>

### <span data-ttu-id="43468-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="43468-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="43468-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43468-141">NOTES</span></span>

## <span data-ttu-id="43468-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43468-142">RELATED LINKS</span></span>
