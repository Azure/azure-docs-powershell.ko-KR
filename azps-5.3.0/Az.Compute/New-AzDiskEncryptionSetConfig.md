---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493842"
---
# <span data-ttu-id="76c56-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="76c56-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="76c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c56-102">SYNOPSIS</span></span>
<span data-ttu-id="76c56-103">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="76c56-104">구문</span><span class="sxs-lookup"><span data-stu-id="76c56-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c56-105">설명</span><span class="sxs-lookup"><span data-stu-id="76c56-105">DESCRIPTION</span></span>
<span data-ttu-id="76c56-106">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="76c56-107">예제</span><span class="sxs-lookup"><span data-stu-id="76c56-107">EXAMPLES</span></span>

### <span data-ttu-id="76c56-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="76c56-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="76c56-109">키 자격 증명 모음에 제공된 활성 키를 사용하여 디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="76c56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76c56-110">PARAMETERS</span></span>

### <span data-ttu-id="76c56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c56-111">-DefaultProfile</span></span>
<span data-ttu-id="76c56-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c56-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="76c56-113">-EncryptionType</span></span>
<span data-ttu-id="76c56-114">디스크 암호화 집합의 암호화 유형을 설정하는 데 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="76c56-115">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c56-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="76c56-116">-IdentityType</span></span>
<span data-ttu-id="76c56-117">DiskEncryptionSet에서 사용하는 관리 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="76c56-118">SystemAssigned만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-118">Only SystemAssigned is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c56-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="76c56-119">-KeyUrl</span></span>
<span data-ttu-id="76c56-120">KeyVault에서 활성 키를 참조하는 URL</span><span class="sxs-lookup"><span data-stu-id="76c56-120">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c56-121">-Location</span><span class="sxs-lookup"><span data-stu-id="76c56-121">-Location</span></span>
<span data-ttu-id="76c56-122">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-122">Specifies a location.</span></span>

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

### <span data-ttu-id="76c56-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="76c56-123">-SourceVaultId</span></span>
<span data-ttu-id="76c56-124">활성 키를 포함하는 KeyVault의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c56-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="76c56-125">-Tag</span></span>
<span data-ttu-id="76c56-126">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="76c56-127">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="76c56-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c56-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76c56-128">-Confirm</span></span>
<span data-ttu-id="76c56-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c56-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c56-130">-WhatIf</span></span>
<span data-ttu-id="76c56-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="76c56-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c56-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c56-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c56-133">CommonParameters</span></span>
<span data-ttu-id="76c56-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76c56-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c56-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76c56-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c56-136">입력</span><span class="sxs-lookup"><span data-stu-id="76c56-136">INPUTS</span></span>

### <span data-ttu-id="76c56-137">System.String</span><span class="sxs-lookup"><span data-stu-id="76c56-137">System.String</span></span>

### <span data-ttu-id="76c56-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="76c56-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76c56-139">출력</span><span class="sxs-lookup"><span data-stu-id="76c56-139">OUTPUTS</span></span>

### <span data-ttu-id="76c56-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="76c56-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="76c56-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76c56-141">NOTES</span></span>

## <span data-ttu-id="76c56-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76c56-142">RELATED LINKS</span></span>
