---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: c427c63e6d7e954e2ce832b3d6e5fe3bf7c4a851
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876898"
---
# <span data-ttu-id="a2ebc-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a2ebc-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="a2ebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ebc-103">스냅샷 업데이트 개체의 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="a2ebc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2ebc-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2ebc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ebc-106">**AzSnapshotUpdateDiskEncryptionKey** cmdlet은 스냅숏 업데이트 개체의 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="a2ebc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="a2ebc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2ebc-108">Example 1</span></span>
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

<span data-ttu-id="a2ebc-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a2ebc-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a2ebc-111">두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="a2ebc-112">마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a2ebc-113">변수</span><span class="sxs-lookup"><span data-stu-id="a2ebc-113">PARAMETERS</span></span>

### <span data-ttu-id="a2ebc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ebc-114">-DefaultProfile</span></span>
<span data-ttu-id="a2ebc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ebc-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="a2ebc-116">-SecretUrl</span></span>
<span data-ttu-id="a2ebc-117">비밀 Url을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-117">Specifes the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ebc-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a2ebc-118">-SnapshotUpdate</span></span>
<span data-ttu-id="a2ebc-119">로컬 스냅숏 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ebc-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a2ebc-120">-SourceVaultId</span></span>
<span data-ttu-id="a2ebc-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ebc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a2ebc-122">-Confirm</span></span>
<span data-ttu-id="a2ebc-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ebc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ebc-124">-WhatIf</span></span>
<span data-ttu-id="a2ebc-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ebc-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ebc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ebc-127">CommonParameters</span></span>
<span data-ttu-id="a2ebc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ebc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ebc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ebc-130">입력</span><span class="sxs-lookup"><span data-stu-id="a2ebc-130">INPUTS</span></span>

### <span data-ttu-id="a2ebc-131">SnapshotUpdate를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="a2ebc-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2ebc-132">System.String</span></span>

## <span data-ttu-id="a2ebc-133">출력</span><span class="sxs-lookup"><span data-stu-id="a2ebc-133">OUTPUTS</span></span>

### <span data-ttu-id="a2ebc-134">SnapshotUpdate를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ebc-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="a2ebc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a2ebc-135">NOTES</span></span>

## <span data-ttu-id="a2ebc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2ebc-136">RELATED LINKS</span></span>

