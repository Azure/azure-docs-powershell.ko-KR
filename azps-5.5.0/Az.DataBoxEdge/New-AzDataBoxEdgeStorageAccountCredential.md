---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196617"
---
# <span data-ttu-id="006fa-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="006fa-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="006fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="006fa-102">SYNOPSIS</span></span>
<span data-ttu-id="006fa-103">디바이스에서 에지 저장소 계정에 대한 새 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="006fa-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="006fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="006fa-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="006fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="006fa-105">DESCRIPTION</span></span>
<span data-ttu-id="006fa-106">**New-AzDataBoxEdgeStorageAccountCredential** cmdlet은 Data Box Edge 디바이스에 대한 새 에지 저장소 계정 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="006fa-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="006fa-107">예제</span><span class="sxs-lookup"><span data-stu-id="006fa-107">EXAMPLES</span></span>

### <span data-ttu-id="006fa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="006fa-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="006fa-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="006fa-109">PARAMETERS</span></span>

### <span data-ttu-id="006fa-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="006fa-110">-AsJob</span></span>
<span data-ttu-id="006fa-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="006fa-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="006fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006fa-112">-DefaultProfile</span></span>
<span data-ttu-id="006fa-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="006fa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="006fa-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="006fa-114">-DeviceName</span></span>
<span data-ttu-id="006fa-115">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="006fa-115">Device Name</span></span>

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

### <span data-ttu-id="006fa-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="006fa-116">-EncryptionKey</span></span>
<span data-ttu-id="006fa-117">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="006fa-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="006fa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="006fa-118">-Name</span></span>
<span data-ttu-id="006fa-119">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="006fa-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="006fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="006fa-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="006fa-121">Resource Group Name</span></span>

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

### <span data-ttu-id="006fa-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="006fa-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="006fa-123">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="006fa-123">provide storage account access key</span></span>

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

### <span data-ttu-id="006fa-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="006fa-124">-StorageAccountType</span></span>
<span data-ttu-id="006fa-125">가능한 저장소 액세스 유형 GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="006fa-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="006fa-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="006fa-126">-Confirm</span></span>
<span data-ttu-id="006fa-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="006fa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="006fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="006fa-128">-WhatIf</span></span>
<span data-ttu-id="006fa-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="006fa-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="006fa-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="006fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="006fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006fa-131">CommonParameters</span></span>
<span data-ttu-id="006fa-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="006fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006fa-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="006fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006fa-134">입력</span><span class="sxs-lookup"><span data-stu-id="006fa-134">INPUTS</span></span>

### <span data-ttu-id="006fa-135">없음</span><span class="sxs-lookup"><span data-stu-id="006fa-135">None</span></span>

## <span data-ttu-id="006fa-136">출력</span><span class="sxs-lookup"><span data-stu-id="006fa-136">OUTPUTS</span></span>

### <span data-ttu-id="006fa-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="006fa-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="006fa-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="006fa-138">NOTES</span></span>

## <span data-ttu-id="006fa-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="006fa-139">RELATED LINKS</span></span>
