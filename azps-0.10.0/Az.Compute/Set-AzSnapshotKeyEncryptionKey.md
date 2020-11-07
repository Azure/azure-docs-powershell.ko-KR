---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 5812bdf70a7661603aad60ece9577926ef10ffb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876902"
---
# <span data-ttu-id="cc68e-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cc68e-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="cc68e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc68e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc68e-103">Snapshot 개체에 대 한 키 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="cc68e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc68e-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc68e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc68e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc68e-106">**Set-AzSnapshotKeyEncryptionKey** cmdlet은 snapshot 개체에 대 한 키 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="cc68e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cc68e-107">EXAMPLES</span></span>

### <span data-ttu-id="cc68e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc68e-108">Example 1</span></span>
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

<span data-ttu-id="cc68e-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="cc68e-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cc68e-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="cc68e-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cc68e-113">변수</span><span class="sxs-lookup"><span data-stu-id="cc68e-113">PARAMETERS</span></span>

### <span data-ttu-id="cc68e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc68e-114">-DefaultProfile</span></span>
<span data-ttu-id="cc68e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc68e-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="cc68e-116">-KeyUrl</span></span>
<span data-ttu-id="cc68e-117">키 Url을 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="cc68e-118">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="cc68e-118">-Snapshot</span></span>
<span data-ttu-id="cc68e-119">로컬 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc68e-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="cc68e-120">-SourceVaultId</span></span>
<span data-ttu-id="cc68e-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="cc68e-122">-확인</span><span class="sxs-lookup"><span data-stu-id="cc68e-122">-Confirm</span></span>
<span data-ttu-id="cc68e-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc68e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc68e-124">-WhatIf</span></span>
<span data-ttu-id="cc68e-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc68e-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc68e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc68e-127">CommonParameters</span></span>
<span data-ttu-id="cc68e-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc68e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc68e-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc68e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc68e-130">입력</span><span class="sxs-lookup"><span data-stu-id="cc68e-130">INPUTS</span></span>

### <span data-ttu-id="cc68e-131">Microsoft. 관리. 스냅샷</span><span class="sxs-lookup"><span data-stu-id="cc68e-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="cc68e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc68e-132">System.String</span></span>

## <span data-ttu-id="cc68e-133">출력</span><span class="sxs-lookup"><span data-stu-id="cc68e-133">OUTPUTS</span></span>

### <span data-ttu-id="cc68e-134">Microsoft. 관리. 스냅샷</span><span class="sxs-lookup"><span data-stu-id="cc68e-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="cc68e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="cc68e-135">NOTES</span></span>

## <span data-ttu-id="cc68e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc68e-136">RELATED LINKS</span></span>

