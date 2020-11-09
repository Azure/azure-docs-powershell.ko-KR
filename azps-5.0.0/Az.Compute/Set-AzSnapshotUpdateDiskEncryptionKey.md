---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304331"
---
# <span data-ttu-id="b21e6-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b21e6-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="b21e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b21e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b21e6-103">스냅샷 업데이트 개체의 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="b21e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b21e6-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b21e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b21e6-105">DESCRIPTION</span></span>
<span data-ttu-id="b21e6-106">**AzSnapshotUpdateDiskEncryptionKey** cmdlet은 스냅숏 업데이트 개체의 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="b21e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b21e6-107">EXAMPLES</span></span>

### <span data-ttu-id="b21e6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b21e6-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="b21e6-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b21e6-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b21e6-111">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="b21e6-112">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b21e6-113">변수</span><span class="sxs-lookup"><span data-stu-id="b21e6-113">PARAMETERS</span></span>

### <span data-ttu-id="b21e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21e6-114">-DefaultProfile</span></span>
<span data-ttu-id="b21e6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b21e6-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="b21e6-116">-SecretUrl</span></span>
<span data-ttu-id="b21e6-117">비밀 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-117">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b21e6-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b21e6-118">-SnapshotUpdate</span></span>
<span data-ttu-id="b21e6-119">로컬 스냅숏 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b21e6-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b21e6-120">-SourceVaultId</span></span>
<span data-ttu-id="b21e6-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="b21e6-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b21e6-122">-Confirm</span></span>
<span data-ttu-id="b21e6-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21e6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21e6-124">-WhatIf</span></span>
<span data-ttu-id="b21e6-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21e6-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21e6-127">CommonParameters</span></span>
<span data-ttu-id="b21e6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b21e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21e6-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b21e6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21e6-130">입력</span><span class="sxs-lookup"><span data-stu-id="b21e6-130">INPUTS</span></span>

### <span data-ttu-id="b21e6-131">PSSnapshotUpdate의. m a.</span><span class="sxs-lookup"><span data-stu-id="b21e6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="b21e6-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b21e6-132">System.String</span></span>

## <span data-ttu-id="b21e6-133">출력</span><span class="sxs-lookup"><span data-stu-id="b21e6-133">OUTPUTS</span></span>

### <span data-ttu-id="b21e6-134">PSSnapshotUpdate의. m a.</span><span class="sxs-lookup"><span data-stu-id="b21e6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="b21e6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b21e6-135">NOTES</span></span>

## <span data-ttu-id="b21e6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b21e6-136">RELATED LINKS</span></span>
