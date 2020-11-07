---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 399c4030f9cd3efd04ec41ce3ab3475f0a660f4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876801"
---
# <span data-ttu-id="28a5d-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="28a5d-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="28a5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="28a5d-103">장치에서 edge 저장소 계정에 대 한 새 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="28a5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28a5d-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28a5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="28a5d-106">**AzDataBoxEdgeStorageAccountCredential** Cmdlet은 데이터 상자 가장자리 장치에 대 한 새 edge 저장소 계정 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="28a5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="28a5d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="28a5d-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="28a5d-109">변수</span><span class="sxs-lookup"><span data-stu-id="28a5d-109">PARAMETERS</span></span>

### <span data-ttu-id="28a5d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28a5d-110">-AsJob</span></span>
<span data-ttu-id="28a5d-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="28a5d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28a5d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a5d-112">-DefaultProfile</span></span>
<span data-ttu-id="28a5d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a5d-114">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="28a5d-114">-DeviceName</span></span>
<span data-ttu-id="28a5d-115">장치 이름</span><span class="sxs-lookup"><span data-stu-id="28a5d-115">Device Name</span></span>

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

### <span data-ttu-id="28a5d-116">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="28a5d-116">-EncryptionKey</span></span>
<span data-ttu-id="28a5d-117">Edge 장치의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="28a5d-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="28a5d-118">-이름</span><span class="sxs-lookup"><span data-stu-id="28a5d-118">-Name</span></span>
<span data-ttu-id="28a5d-119">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="28a5d-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="28a5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="28a5d-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="28a5d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="28a5d-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="28a5d-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="28a5d-123">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="28a5d-123">provide storage account access key</span></span>

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

### <span data-ttu-id="28a5d-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="28a5d-124">-StorageAccountType</span></span>
<span data-ttu-id="28a5d-125">사용할 수 있는 저장소 액세스 형식 GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="28a5d-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="28a5d-126">-확인</span><span class="sxs-lookup"><span data-stu-id="28a5d-126">-Confirm</span></span>
<span data-ttu-id="28a5d-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a5d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a5d-128">-WhatIf</span></span>
<span data-ttu-id="28a5d-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28a5d-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a5d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a5d-131">CommonParameters</span></span>
<span data-ttu-id="28a5d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a5d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a5d-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28a5d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a5d-134">입력</span><span class="sxs-lookup"><span data-stu-id="28a5d-134">INPUTS</span></span>

### <span data-ttu-id="28a5d-135">않아야</span><span class="sxs-lookup"><span data-stu-id="28a5d-135">None</span></span>

## <span data-ttu-id="28a5d-136">출력</span><span class="sxs-lookup"><span data-stu-id="28a5d-136">OUTPUTS</span></span>

### <span data-ttu-id="28a5d-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="28a5d-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="28a5d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="28a5d-138">NOTES</span></span>

## <span data-ttu-id="28a5d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28a5d-139">RELATED LINKS</span></span>
