---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f73132550eceb092c8c869e7a555173c11d7d226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980880"
---
# <span data-ttu-id="95bac-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="95bac-101">New-AzSnapshot</span></span>

## <span data-ttu-id="95bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95bac-102">SYNOPSIS</span></span>
<span data-ttu-id="95bac-103">스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-103">Creates a snapshot.</span></span>

## <span data-ttu-id="95bac-104">구문</span><span class="sxs-lookup"><span data-stu-id="95bac-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bac-105">설명</span><span class="sxs-lookup"><span data-stu-id="95bac-105">DESCRIPTION</span></span>
<span data-ttu-id="95bac-106">**New-AzSnapshot** cmdlet은 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="95bac-107">예제</span><span class="sxs-lookup"><span data-stu-id="95bac-107">EXAMPLES</span></span>

### <span data-ttu-id="95bac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95bac-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="95bac-109">첫 번째 명령은 저장소 계정 유형에 크기가 5GB인 로컬 빈 스냅숏 개체를 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="95bac-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="95bac-111">두 번째 및 세 번째 명령은 스냅숏 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="95bac-112">마지막 명령은 스냅숏 개체를 만들고 리소스 그룹 'ResourceGroup01'에서 '스냅숏01'을 사용하여 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="95bac-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="95bac-113">PARAMETERS</span></span>

### <span data-ttu-id="95bac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95bac-114">-AsJob</span></span>
<span data-ttu-id="95bac-115">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95bac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bac-116">-DefaultProfile</span></span>
<span data-ttu-id="95bac-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95bac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95bac-118">-ResourceGroupName</span></span>
<span data-ttu-id="95bac-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="95bac-120">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="95bac-120">-Snapshot</span></span>
<span data-ttu-id="95bac-121">로컬 스냅숏 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95bac-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="95bac-122">-SnapshotName</span></span>
<span data-ttu-id="95bac-123">스냅숏의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bac-124">-확인</span><span class="sxs-lookup"><span data-stu-id="95bac-124">-Confirm</span></span>
<span data-ttu-id="95bac-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bac-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bac-126">-WhatIf</span></span>
<span data-ttu-id="95bac-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bac-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bac-129">CommonParameters</span></span>
<span data-ttu-id="95bac-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95bac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bac-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95bac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bac-132">입력</span><span class="sxs-lookup"><span data-stu-id="95bac-132">INPUTS</span></span>

### <span data-ttu-id="95bac-133">System.String</span><span class="sxs-lookup"><span data-stu-id="95bac-133">System.String</span></span>

### <span data-ttu-id="95bac-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="95bac-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="95bac-135">출력</span><span class="sxs-lookup"><span data-stu-id="95bac-135">OUTPUTS</span></span>

### <span data-ttu-id="95bac-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="95bac-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="95bac-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95bac-137">NOTES</span></span>

## <span data-ttu-id="95bac-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95bac-138">RELATED LINKS</span></span>
