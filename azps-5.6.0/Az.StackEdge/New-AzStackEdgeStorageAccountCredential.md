---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: a9bb0e844101c4d21db52c2f7852e3b548d283cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002923"
---
# <span data-ttu-id="7c532-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c532-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7c532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c532-102">SYNOPSIS</span></span>
<span data-ttu-id="7c532-103">디바이스에서 에지 저장소 계정에 대한 새 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="7c532-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c532-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c532-105">설명</span><span class="sxs-lookup"><span data-stu-id="7c532-105">DESCRIPTION</span></span>
<span data-ttu-id="7c532-106">**New-AzStackEdgeStorageAccountCredential** cmdlet은 Stack Edge 디바이스에 대한 새 에지 저장소 계정 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="7c532-107">예제</span><span class="sxs-lookup"><span data-stu-id="7c532-107">EXAMPLES</span></span>

### <span data-ttu-id="7c532-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c532-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="7c532-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c532-109">PARAMETERS</span></span>

### <span data-ttu-id="7c532-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c532-110">-AsJob</span></span>
<span data-ttu-id="7c532-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c532-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c532-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c532-112">-DefaultProfile</span></span>
<span data-ttu-id="7c532-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c532-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7c532-114">-DeviceName</span></span>
<span data-ttu-id="7c532-115">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="7c532-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7c532-116">-EncryptionKey</span></span>
<span data-ttu-id="7c532-117">Edge 디바이스의 암호화 키</span><span class="sxs-lookup"><span data-stu-id="7c532-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="7c532-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7c532-118">-Name</span></span>
<span data-ttu-id="7c532-119">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7c532-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c532-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c532-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7c532-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c532-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="7c532-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="7c532-123">저장소 계정 액세스 키 제공</span><span class="sxs-lookup"><span data-stu-id="7c532-123">provide storage account access key</span></span>

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

### <span data-ttu-id="7c532-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7c532-124">-StorageAccountType</span></span>
<span data-ttu-id="7c532-125">가능한 저장소 액세스 유형 GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="7c532-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="7c532-126">-확인</span><span class="sxs-lookup"><span data-stu-id="7c532-126">-Confirm</span></span>
<span data-ttu-id="7c532-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c532-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c532-128">-WhatIf</span></span>
<span data-ttu-id="7c532-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c532-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c532-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c532-131">CommonParameters</span></span>
<span data-ttu-id="7c532-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c532-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c532-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c532-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c532-134">입력</span><span class="sxs-lookup"><span data-stu-id="7c532-134">INPUTS</span></span>

### <span data-ttu-id="7c532-135">없음</span><span class="sxs-lookup"><span data-stu-id="7c532-135">None</span></span>

## <span data-ttu-id="7c532-136">출력</span><span class="sxs-lookup"><span data-stu-id="7c532-136">OUTPUTS</span></span>

### <span data-ttu-id="7c532-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7c532-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7c532-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c532-138">NOTES</span></span>

## <span data-ttu-id="7c532-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c532-139">RELATED LINKS</span></span>
