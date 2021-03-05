---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: 9a4afaa1a67d9f1f9bffa0fdf6c7b40c7cf72b13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973376"
---
# <span data-ttu-id="c39b8-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c39b8-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c39b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c39b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c39b8-103">Azure Storage Blob 서비스에 대한 삭제 보존 정책을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c39b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="c39b8-104">SYNTAX</span></span>

### <span data-ttu-id="c39b8-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c39b8-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c39b8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c39b8-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39b8-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c39b8-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c39b8-108">설명</span><span class="sxs-lookup"><span data-stu-id="c39b8-108">DESCRIPTION</span></span>
<span data-ttu-id="c39b8-109">**Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet을 사용하면 Azure Storage Blob 서비스에 대한 삭제 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c39b8-110">예제</span><span class="sxs-lookup"><span data-stu-id="c39b8-110">EXAMPLES</span></span>

### <span data-ttu-id="c39b8-111">예제 1: Blob 서비스에 대한 삭제 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="c39b8-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="c39b8-112">이 명령을 사용하면 Blob 서비스에 대한 삭제 보존 정책을 사용할 수 있으며 삭제된 Blob 보존일을 4로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="c39b8-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c39b8-113">PARAMETERS</span></span>

### <span data-ttu-id="c39b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39b8-114">-DefaultProfile</span></span>
<span data-ttu-id="c39b8-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c39b8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c39b8-116">-PassThru</span></span>
<span data-ttu-id="c39b8-117">Display ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c39b8-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="c39b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="c39b8-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c39b8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c39b8-120">-ResourceId</span></span>
<span data-ttu-id="c39b8-121">Storage 계정 리소스 ID 또는 Blob 서비스 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="c39b8-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="c39b8-122">-RetentionDays</span></span>
<span data-ttu-id="c39b8-123">DeleteRetentionPolicy에 대한 보존 일 수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="c39b8-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c39b8-124">-StorageAccount</span></span>
<span data-ttu-id="c39b8-125">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c39b8-125">Storage account object</span></span>

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

### <span data-ttu-id="c39b8-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c39b8-126">-StorageAccountName</span></span>
<span data-ttu-id="c39b8-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="c39b8-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c39b8-128">-Confirm</span></span>
<span data-ttu-id="c39b8-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39b8-130">-WhatIf</span></span>
<span data-ttu-id="c39b8-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39b8-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39b8-133">CommonParameters</span></span>
<span data-ttu-id="c39b8-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c39b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39b8-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c39b8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39b8-136">입력</span><span class="sxs-lookup"><span data-stu-id="c39b8-136">INPUTS</span></span>

### <span data-ttu-id="c39b8-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c39b8-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c39b8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c39b8-138">System.String</span></span>

## <span data-ttu-id="c39b8-139">출력</span><span class="sxs-lookup"><span data-stu-id="c39b8-139">OUTPUTS</span></span>

### <span data-ttu-id="c39b8-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c39b8-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="c39b8-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c39b8-141">NOTES</span></span>

## <span data-ttu-id="c39b8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c39b8-142">RELATED LINKS</span></span>
