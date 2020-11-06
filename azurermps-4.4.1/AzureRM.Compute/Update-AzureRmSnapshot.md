---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: 71407a78dd19f6324370b88be06841918a4c244a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531830"
---
# <span data-ttu-id="05ca4-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="05ca4-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="05ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="05ca4-103">스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05ca4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05ca4-104">SYNTAX</span></span>

### <span data-ttu-id="05ca4-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="05ca4-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <PSSnapshotUpdate> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05ca4-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="05ca4-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ca4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05ca4-107">DESCRIPTION</span></span>
<span data-ttu-id="05ca4-108">**업데이트 AzureRmSnapshot** cmdlet은 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="05ca4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05ca4-109">EXAMPLES</span></span>

### <span data-ttu-id="05ca4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05ca4-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="05ca4-111">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="05ca4-112">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="05ca4-113">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="05ca4-114">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="05ca4-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="05ca4-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="05ca4-116">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="05ca4-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="05ca4-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="05ca4-118">또한이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅샷을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="05ca4-119">변수</span><span class="sxs-lookup"><span data-stu-id="05ca4-119">PARAMETERS</span></span>

### <span data-ttu-id="05ca4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ca4-120">-DefaultProfile</span></span>
<span data-ttu-id="05ca4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ca4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ca4-122">-ResourceGroupName</span></span>
<span data-ttu-id="05ca4-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="05ca4-124">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="05ca4-124">-Snapshot</span></span>
<span data-ttu-id="05ca4-125">로컬 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-125">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ca4-126">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="05ca4-126">-SnapshotName</span></span>
<span data-ttu-id="05ca4-127">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-127">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ca4-128">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="05ca4-128">-SnapshotUpdate</span></span>
<span data-ttu-id="05ca4-129">로컬 스냅숏 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-129">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ca4-130">-확인</span><span class="sxs-lookup"><span data-stu-id="05ca4-130">-Confirm</span></span>
<span data-ttu-id="05ca4-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ca4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ca4-132">-WhatIf</span></span>
<span data-ttu-id="05ca4-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ca4-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ca4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ca4-135">CommonParameters</span></span>
<span data-ttu-id="05ca4-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ca4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ca4-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ca4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ca4-138">입력</span><span class="sxs-lookup"><span data-stu-id="05ca4-138">INPUTS</span></span>

### <span data-ttu-id="05ca4-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05ca4-139">System.String</span></span>
<span data-ttu-id="05ca4-140">SnapshotUpdate. 관리. a. i. i m a. 스냅샷</span><span class="sxs-lookup"><span data-stu-id="05ca4-140">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="05ca4-141">출력</span><span class="sxs-lookup"><span data-stu-id="05ca4-141">OUTPUTS</span></span>

### <span data-ttu-id="05ca4-142">System. 개체</span><span class="sxs-lookup"><span data-stu-id="05ca4-142">System.Object</span></span>

## <span data-ttu-id="05ca4-143">상속자</span><span class="sxs-lookup"><span data-stu-id="05ca4-143">NOTES</span></span>

## <span data-ttu-id="05ca4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05ca4-144">RELATED LINKS</span></span>

