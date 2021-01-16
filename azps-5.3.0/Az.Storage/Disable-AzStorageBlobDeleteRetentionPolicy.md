---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374165"
---
# <span data-ttu-id="36bc8-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36bc8-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="36bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="36bc8-103">Azure Storage Blob service에 대한 삭제 보존 정책을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="36bc8-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="36bc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="36bc8-104">SYNTAX</span></span>

### <span data-ttu-id="36bc8-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="36bc8-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="36bc8-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36bc8-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="36bc8-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36bc8-108">설명</span><span class="sxs-lookup"><span data-stu-id="36bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="36bc8-109">**Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet은 Azure Storage Blob service에 대한 삭제 보존 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="36bc8-110">예제</span><span class="sxs-lookup"><span data-stu-id="36bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="36bc8-111">예제 1: Blob service에 대한 삭제 보존 정책 사용 안</span><span class="sxs-lookup"><span data-stu-id="36bc8-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="36bc8-112">이 명령은 Blob service에 대한 삭제 보존 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="36bc8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36bc8-113">PARAMETERS</span></span>

### <span data-ttu-id="36bc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bc8-114">-DefaultProfile</span></span>
<span data-ttu-id="36bc8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36bc8-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36bc8-116">-PassThru</span></span>
<span data-ttu-id="36bc8-117">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="36bc8-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="36bc8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bc8-118">-ResourceGroupName</span></span>
<span data-ttu-id="36bc8-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="36bc8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36bc8-120">-ResourceId</span></span>
<span data-ttu-id="36bc8-121">Storage 계정 리소스 ID 또는 Blob service 속성 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="36bc8-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="36bc8-122">-StorageAccount</span></span>
<span data-ttu-id="36bc8-123">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="36bc8-123">Storage account object</span></span>

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

### <span data-ttu-id="36bc8-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="36bc8-124">-StorageAccountName</span></span>
<span data-ttu-id="36bc8-125">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="36bc8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36bc8-126">-Confirm</span></span>
<span data-ttu-id="36bc8-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36bc8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36bc8-128">-WhatIf</span></span>
<span data-ttu-id="36bc8-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="36bc8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36bc8-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36bc8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bc8-131">CommonParameters</span></span>
<span data-ttu-id="36bc8-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36bc8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bc8-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36bc8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bc8-134">입력</span><span class="sxs-lookup"><span data-stu-id="36bc8-134">INPUTS</span></span>

### <span data-ttu-id="36bc8-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36bc8-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="36bc8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="36bc8-136">System.String</span></span>

## <span data-ttu-id="36bc8-137">출력</span><span class="sxs-lookup"><span data-stu-id="36bc8-137">OUTPUTS</span></span>

### <span data-ttu-id="36bc8-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36bc8-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="36bc8-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36bc8-139">NOTES</span></span>

## <span data-ttu-id="36bc8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36bc8-140">RELATED LINKS</span></span>