---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216247"
---
# <span data-ttu-id="237ae-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="237ae-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="237ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="237ae-102">SYNOPSIS</span></span>
<span data-ttu-id="237ae-103">디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="237ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="237ae-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="237ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="237ae-105">DESCRIPTION</span></span>
<span data-ttu-id="237ae-106">디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="237ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="237ae-107">EXAMPLES</span></span>

### <span data-ttu-id="237ae-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="237ae-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="237ae-109">키 자격 증명 모음에서 지정 된 활성 키를 사용 하 여 디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="237ae-110">변수</span><span class="sxs-lookup"><span data-stu-id="237ae-110">PARAMETERS</span></span>

### <span data-ttu-id="237ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="237ae-111">-AsJob</span></span>
<span data-ttu-id="237ae-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="237ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="237ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237ae-113">-DefaultProfile</span></span>
<span data-ttu-id="237ae-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="237ae-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="237ae-115">-InputObject</span></span>
<span data-ttu-id="237ae-116">디스크 암호화 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="237ae-117">-이름</span><span class="sxs-lookup"><span data-stu-id="237ae-117">-Name</span></span>
<span data-ttu-id="237ae-118">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="237ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="237ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="237ae-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="237ae-121">-확인</span><span class="sxs-lookup"><span data-stu-id="237ae-121">-Confirm</span></span>
<span data-ttu-id="237ae-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="237ae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="237ae-123">-WhatIf</span></span>
<span data-ttu-id="237ae-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="237ae-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="237ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237ae-126">CommonParameters</span></span>
<span data-ttu-id="237ae-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="237ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237ae-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="237ae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237ae-129">입력</span><span class="sxs-lookup"><span data-stu-id="237ae-129">INPUTS</span></span>

### <span data-ttu-id="237ae-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="237ae-130">System.String</span></span>

### <span data-ttu-id="237ae-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="237ae-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="237ae-132">출력</span><span class="sxs-lookup"><span data-stu-id="237ae-132">OUTPUTS</span></span>

### <span data-ttu-id="237ae-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="237ae-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="237ae-134">상속자</span><span class="sxs-lookup"><span data-stu-id="237ae-134">NOTES</span></span>

## <span data-ttu-id="237ae-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="237ae-135">RELATED LINKS</span></span>
