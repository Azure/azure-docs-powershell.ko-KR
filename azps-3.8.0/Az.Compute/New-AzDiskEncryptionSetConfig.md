---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034929"
---
# <span data-ttu-id="54c38-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="54c38-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="54c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c38-102">SYNOPSIS</span></span>
<span data-ttu-id="54c38-103">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="54c38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54c38-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54c38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54c38-105">DESCRIPTION</span></span>
<span data-ttu-id="54c38-106">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="54c38-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54c38-107">EXAMPLES</span></span>

### <span data-ttu-id="54c38-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="54c38-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="54c38-109">키 자격 증명 모음에서 지정 된 활성 키를 사용 하 여 디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="54c38-110">변수</span><span class="sxs-lookup"><span data-stu-id="54c38-110">PARAMETERS</span></span>

### <span data-ttu-id="54c38-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c38-111">-DefaultProfile</span></span>
<span data-ttu-id="54c38-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c38-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="54c38-113">-IdentityType</span></span>
<span data-ttu-id="54c38-114">Diska Set에 사용 되는 관리 되는 Id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="54c38-115">할당 된 시스템만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="54c38-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="54c38-116">-KeyUrl</span></span>
<span data-ttu-id="54c38-117">KeyVault의 활성 키를 가리키는 Url</span><span class="sxs-lookup"><span data-stu-id="54c38-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="54c38-118">-위치</span><span class="sxs-lookup"><span data-stu-id="54c38-118">-Location</span></span>
<span data-ttu-id="54c38-119">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-119">Specifies a location.</span></span>

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

### <span data-ttu-id="54c38-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="54c38-120">-SourceVaultId</span></span>
<span data-ttu-id="54c38-121">활성 키를 포함 하는 KeyVault의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="54c38-122">태그</span><span class="sxs-lookup"><span data-stu-id="54c38-122">-Tag</span></span>
<span data-ttu-id="54c38-123">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="54c38-124">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="54c38-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="54c38-125">-확인</span><span class="sxs-lookup"><span data-stu-id="54c38-125">-Confirm</span></span>
<span data-ttu-id="54c38-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c38-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c38-127">-WhatIf</span></span>
<span data-ttu-id="54c38-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c38-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c38-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c38-130">CommonParameters</span></span>
<span data-ttu-id="54c38-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54c38-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c38-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54c38-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c38-133">입력</span><span class="sxs-lookup"><span data-stu-id="54c38-133">INPUTS</span></span>

### <span data-ttu-id="54c38-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="54c38-134">System.String</span></span>

### <span data-ttu-id="54c38-135">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="54c38-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="54c38-136">출력</span><span class="sxs-lookup"><span data-stu-id="54c38-136">OUTPUTS</span></span>

### <span data-ttu-id="54c38-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="54c38-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="54c38-138">상속자</span><span class="sxs-lookup"><span data-stu-id="54c38-138">NOTES</span></span>

## <span data-ttu-id="54c38-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54c38-139">RELATED LINKS</span></span>
