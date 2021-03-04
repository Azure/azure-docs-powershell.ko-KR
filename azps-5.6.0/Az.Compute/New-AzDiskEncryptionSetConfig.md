---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 358481a4c8ba20e8c8aa6f2ed47ebaa13225b939
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957600"
---
# <span data-ttu-id="df80c-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="df80c-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="df80c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df80c-102">SYNOPSIS</span></span>
<span data-ttu-id="df80c-103">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="df80c-104">구문</span><span class="sxs-lookup"><span data-stu-id="df80c-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df80c-105">설명</span><span class="sxs-lookup"><span data-stu-id="df80c-105">DESCRIPTION</span></span>
<span data-ttu-id="df80c-106">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="df80c-107">예제</span><span class="sxs-lookup"><span data-stu-id="df80c-107">EXAMPLES</span></span>

### <span data-ttu-id="df80c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="df80c-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="df80c-109">키 자격 증명 모음에서 주어진 활성 키를 사용하여 디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="df80c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="df80c-110">PARAMETERS</span></span>

### <span data-ttu-id="df80c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df80c-111">-DefaultProfile</span></span>
<span data-ttu-id="df80c-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df80c-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="df80c-113">-EncryptionType</span></span>
<span data-ttu-id="df80c-114">이 기능을 사용하여 디스크 암호화 집합의 암호화 유형을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="df80c-115">사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="df80c-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="df80c-116">-IdentityType</span></span>
<span data-ttu-id="df80c-117">DiskEncryptionSet에서 사용하는 관리 ID의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="df80c-118">SystemAssigned만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="df80c-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="df80c-119">-KeyUrl</span></span>
<span data-ttu-id="df80c-120">KeyVault의 활성 키를 지적하는 URL</span><span class="sxs-lookup"><span data-stu-id="df80c-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="df80c-121">-Location</span><span class="sxs-lookup"><span data-stu-id="df80c-121">-Location</span></span>
<span data-ttu-id="df80c-122">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-122">Specifies a location.</span></span>

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

### <span data-ttu-id="df80c-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="df80c-123">-SourceVaultId</span></span>
<span data-ttu-id="df80c-124">활성 키를 포함하는 KeyVault의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-124">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="df80c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="df80c-125">-Tag</span></span>
<span data-ttu-id="df80c-126">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="df80c-127">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="df80c-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="df80c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="df80c-128">-Confirm</span></span>
<span data-ttu-id="df80c-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df80c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df80c-130">-WhatIf</span></span>
<span data-ttu-id="df80c-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df80c-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df80c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df80c-133">CommonParameters</span></span>
<span data-ttu-id="df80c-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df80c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df80c-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df80c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df80c-136">입력</span><span class="sxs-lookup"><span data-stu-id="df80c-136">INPUTS</span></span>

### <span data-ttu-id="df80c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="df80c-137">System.String</span></span>

### <span data-ttu-id="df80c-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="df80c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df80c-139">출력</span><span class="sxs-lookup"><span data-stu-id="df80c-139">OUTPUTS</span></span>

### <span data-ttu-id="df80c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="df80c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="df80c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df80c-141">NOTES</span></span>

## <span data-ttu-id="df80c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df80c-142">RELATED LINKS</span></span>
