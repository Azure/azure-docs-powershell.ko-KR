---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: 8ffae2b8b68545cd086fb98a7abc42430fdeb927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697367"
---
# <span data-ttu-id="79512-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="79512-101">New-AzSnapshot</span></span>

## <span data-ttu-id="79512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79512-102">SYNOPSIS</span></span>
<span data-ttu-id="79512-103">스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79512-103">Creates a snapshot.</span></span>

## <span data-ttu-id="79512-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79512-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79512-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79512-105">DESCRIPTION</span></span>
<span data-ttu-id="79512-106">**AzSnapshot** cmdlet은 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79512-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="79512-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79512-107">EXAMPLES</span></span>

### <span data-ttu-id="79512-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79512-108">Example 1</span></span>
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

<span data-ttu-id="79512-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79512-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="79512-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="79512-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="79512-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79512-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="79512-113">변수</span><span class="sxs-lookup"><span data-stu-id="79512-113">PARAMETERS</span></span>

### <span data-ttu-id="79512-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79512-114">-AsJob</span></span>
<span data-ttu-id="79512-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="79512-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79512-116">-DefaultProfile</span></span>
<span data-ttu-id="79512-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79512-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79512-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79512-118">-ResourceGroupName</span></span>
<span data-ttu-id="79512-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="79512-120">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="79512-120">-Snapshot</span></span>
<span data-ttu-id="79512-121">로컬 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="79512-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="79512-122">-SnapshotName</span></span>
<span data-ttu-id="79512-123">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="79512-124">-확인</span><span class="sxs-lookup"><span data-stu-id="79512-124">-Confirm</span></span>
<span data-ttu-id="79512-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79512-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79512-126">-WhatIf</span></span>
<span data-ttu-id="79512-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79512-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79512-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79512-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79512-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79512-129">CommonParameters</span></span>
<span data-ttu-id="79512-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79512-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79512-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79512-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79512-132">입력</span><span class="sxs-lookup"><span data-stu-id="79512-132">INPUTS</span></span>

### <span data-ttu-id="79512-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79512-133">System.String</span></span>

### <span data-ttu-id="79512-134">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="79512-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="79512-135">출력</span><span class="sxs-lookup"><span data-stu-id="79512-135">OUTPUTS</span></span>

### <span data-ttu-id="79512-136">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="79512-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="79512-137">상속자</span><span class="sxs-lookup"><span data-stu-id="79512-137">NOTES</span></span>

## <span data-ttu-id="79512-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79512-138">RELATED LINKS</span></span>
