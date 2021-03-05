---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 23fe08b273b95cd5ad3866437d131f432e6cee38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978587"
---
# <span data-ttu-id="d3a9c-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d3a9c-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d3a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a9c-103">디바이스에서 에지 저장소 계정에 대한 새 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="d3a9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3a9c-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a9c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d3a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a9c-106">**New-AzDataBoxEdgeStorageAccountCredential** cmdlet은 Data Box Edge 디바이스에 대한 새 에지 저장소 계정 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="d3a9c-107">예제</span><span class="sxs-lookup"><span data-stu-id="d3a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a9c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3a9c-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="d3a9c-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3a9c-109">PARAMETERS</span></span>

### <span data-ttu-id="d3a9c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3a9c-110">-AsJob</span></span>
<span data-ttu-id="d3a9c-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3a9c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3a9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a9c-112">-DefaultProfile</span></span>
<span data-ttu-id="d3a9c-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a9c-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d3a9c-114">-DeviceName</span></span>
<span data-ttu-id="d3a9c-115">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="d3a9c-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a9c-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d3a9c-116">-EncryptionKey</span></span>
<span data-ttu-id="d3a9c-117">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="d3a9c-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a9c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d3a9c-118">-Name</span></span>
<span data-ttu-id="d3a9c-119">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="d3a9c-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3a9c-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d3a9c-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a9c-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="d3a9c-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="d3a9c-123">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="d3a9c-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a9c-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d3a9c-124">-StorageAccountType</span></span>
<span data-ttu-id="d3a9c-125">가능한 저장소 액세스 유형 GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="d3a9c-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a9c-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d3a9c-126">-Confirm</span></span>
<span data-ttu-id="d3a9c-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a9c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a9c-128">-WhatIf</span></span>
<span data-ttu-id="d3a9c-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3a9c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a9c-131">CommonParameters</span></span>
<span data-ttu-id="d3a9c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a9c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a9c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a9c-134">입력</span><span class="sxs-lookup"><span data-stu-id="d3a9c-134">INPUTS</span></span>

### <span data-ttu-id="d3a9c-135">없음</span><span class="sxs-lookup"><span data-stu-id="d3a9c-135">None</span></span>

## <span data-ttu-id="d3a9c-136">출력</span><span class="sxs-lookup"><span data-stu-id="d3a9c-136">OUTPUTS</span></span>

### <span data-ttu-id="d3a9c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d3a9c-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d3a9c-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3a9c-138">NOTES</span></span>

## <span data-ttu-id="d3a9c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3a9c-139">RELATED LINKS</span></span>
