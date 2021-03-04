---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 3e2e04e2e489b9c9322c62d1c7006490d7bf9bd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957611"
---
# <span data-ttu-id="7f4c0-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7f4c0-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="7f4c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4c0-103">디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="7f4c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f4c0-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f4c0-105">설명</span><span class="sxs-lookup"><span data-stu-id="7f4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="7f4c0-106">디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="7f4c0-107">예제</span><span class="sxs-lookup"><span data-stu-id="7f4c0-107">EXAMPLES</span></span>

### <span data-ttu-id="7f4c0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f4c0-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="7f4c0-109">키 자격 증명 모음에서 주어진 활성 키를 사용하여 디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="7f4c0-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f4c0-110">PARAMETERS</span></span>

### <span data-ttu-id="7f4c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f4c0-111">-AsJob</span></span>
<span data-ttu-id="7f4c0-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7f4c0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f4c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4c0-113">-DefaultProfile</span></span>
<span data-ttu-id="7f4c0-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f4c0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f4c0-115">-InputObject</span></span>
<span data-ttu-id="7f4c0-116">디스크 암호화 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4c0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7f4c0-117">-Name</span></span>
<span data-ttu-id="7f4c0-118">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f4c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f4c0-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7f4c0-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7f4c0-121">-Confirm</span></span>
<span data-ttu-id="7f4c0-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f4c0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f4c0-123">-WhatIf</span></span>
<span data-ttu-id="7f4c0-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f4c0-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f4c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4c0-126">CommonParameters</span></span>
<span data-ttu-id="7f4c0-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f4c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4c0-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f4c0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4c0-129">입력</span><span class="sxs-lookup"><span data-stu-id="7f4c0-129">INPUTS</span></span>

### <span data-ttu-id="7f4c0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7f4c0-130">System.String</span></span>

### <span data-ttu-id="7f4c0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7f4c0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7f4c0-132">출력</span><span class="sxs-lookup"><span data-stu-id="7f4c0-132">OUTPUTS</span></span>

### <span data-ttu-id="7f4c0-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7f4c0-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="7f4c0-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f4c0-134">NOTES</span></span>

## <span data-ttu-id="7f4c0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f4c0-135">RELATED LINKS</span></span>
