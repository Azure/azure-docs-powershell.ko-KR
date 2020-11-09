---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304196"
---
# <span data-ttu-id="13654-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="13654-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="13654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13654-102">SYNOPSIS</span></span>
<span data-ttu-id="13654-103">디스크 암호화 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="13654-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="13654-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13654-104">SYNTAX</span></span>

### <span data-ttu-id="13654-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="13654-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13654-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="13654-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13654-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="13654-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13654-108">설명은</span><span class="sxs-lookup"><span data-stu-id="13654-108">DESCRIPTION</span></span>
<span data-ttu-id="13654-109">디스크 암호화 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="13654-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="13654-110">예제의</span><span class="sxs-lookup"><span data-stu-id="13654-110">EXAMPLES</span></span>

### <span data-ttu-id="13654-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="13654-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="13654-112">키 자격 증명 모음에서 지정 된 활성 키를 사용 하 여 디스크 암호화 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="13654-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="13654-113">변수</span><span class="sxs-lookup"><span data-stu-id="13654-113">PARAMETERS</span></span>

### <span data-ttu-id="13654-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13654-114">-AsJob</span></span>
<span data-ttu-id="13654-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="13654-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13654-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13654-116">-DefaultProfile</span></span>
<span data-ttu-id="13654-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13654-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13654-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13654-118">-InputObject</span></span>
<span data-ttu-id="13654-119">디스크 암호화 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13654-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13654-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="13654-120">-KeyUrl</span></span>
<span data-ttu-id="13654-121">KeyVault의 활성 키를 가리키는 Url</span><span class="sxs-lookup"><span data-stu-id="13654-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="13654-122">-이름</span><span class="sxs-lookup"><span data-stu-id="13654-122">-Name</span></span>
<span data-ttu-id="13654-123">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13654-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13654-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13654-124">-ResourceGroupName</span></span>
<span data-ttu-id="13654-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13654-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13654-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13654-126">-ResourceId</span></span>
<span data-ttu-id="13654-127">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13654-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13654-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="13654-128">-SourceVaultId</span></span>
<span data-ttu-id="13654-129">활성 키를 포함 하는 KeyVault의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="13654-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="13654-130">태그</span><span class="sxs-lookup"><span data-stu-id="13654-130">-Tag</span></span>
<span data-ttu-id="13654-131">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="13654-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="13654-132">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="13654-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="13654-133">-확인</span><span class="sxs-lookup"><span data-stu-id="13654-133">-Confirm</span></span>
<span data-ttu-id="13654-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13654-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13654-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13654-135">-WhatIf</span></span>
<span data-ttu-id="13654-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13654-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13654-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13654-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13654-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13654-138">CommonParameters</span></span>
<span data-ttu-id="13654-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13654-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13654-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13654-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13654-141">입력</span><span class="sxs-lookup"><span data-stu-id="13654-141">INPUTS</span></span>

### <span data-ttu-id="13654-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13654-142">System.String</span></span>

### <span data-ttu-id="13654-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="13654-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="13654-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="13654-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="13654-145">출력</span><span class="sxs-lookup"><span data-stu-id="13654-145">OUTPUTS</span></span>

### <span data-ttu-id="13654-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="13654-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="13654-147">상속자</span><span class="sxs-lookup"><span data-stu-id="13654-147">NOTES</span></span>

## <span data-ttu-id="13654-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13654-148">RELATED LINKS</span></span>
