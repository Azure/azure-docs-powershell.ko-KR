---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: b086703ba8466c6d67e297002e2127a092175c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874063"
---
# <span data-ttu-id="0ab5c-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0ab5c-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="0ab5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab5c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab5c-103">Azure 저장소 Blob 서비스에 대해 보존 정책 삭제를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0ab5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ab5c-104">SYNTAX</span></span>

### <span data-ttu-id="0ab5c-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ab5c-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ab5c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0ab5c-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ab5c-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="0ab5c-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab5c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0ab5c-108">DESCRIPTION</span></span>
<span data-ttu-id="0ab5c-109">**AzStorageBlobDeleteRetentionPolicy** Cmdlet은 Azure Storage Blob service에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0ab5c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0ab5c-110">EXAMPLES</span></span>

### <span data-ttu-id="0ab5c-111">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="0ab5c-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="0ab5c-112">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="0ab5c-113">변수</span><span class="sxs-lookup"><span data-stu-id="0ab5c-113">PARAMETERS</span></span>

### <span data-ttu-id="0ab5c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab5c-114">-DefaultProfile</span></span>
<span data-ttu-id="0ab5c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab5c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ab5c-116">-PassThru</span></span>
<span data-ttu-id="0ab5c-117">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="0ab5c-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="0ab5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="0ab5c-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="0ab5c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ab5c-120">-ResourceId</span></span>
<span data-ttu-id="0ab5c-121">저장소 계정 리소스 Id 또는 Blob 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="0ab5c-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ab5c-122">-StorageAccount</span></span>
<span data-ttu-id="0ab5c-123">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="0ab5c-123">Storage account object</span></span>

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

### <span data-ttu-id="0ab5c-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ab5c-124">-StorageAccountName</span></span>
<span data-ttu-id="0ab5c-125">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="0ab5c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="0ab5c-126">-Confirm</span></span>
<span data-ttu-id="0ab5c-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab5c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab5c-128">-WhatIf</span></span>
<span data-ttu-id="0ab5c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ab5c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab5c-131">CommonParameters</span></span>
<span data-ttu-id="0ab5c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab5c-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab5c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab5c-134">입력</span><span class="sxs-lookup"><span data-stu-id="0ab5c-134">INPUTS</span></span>

### <span data-ttu-id="0ab5c-135">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0ab5c-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0ab5c-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0ab5c-136">System.String</span></span>

## <span data-ttu-id="0ab5c-137">출력</span><span class="sxs-lookup"><span data-stu-id="0ab5c-137">OUTPUTS</span></span>

### <span data-ttu-id="0ab5c-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0ab5c-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="0ab5c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0ab5c-139">NOTES</span></span>

## <span data-ttu-id="0ab5c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ab5c-140">RELATED LINKS</span></span>
