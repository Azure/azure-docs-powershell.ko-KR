---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215591"
---
# <span data-ttu-id="ab6ab-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ab6ab-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="ab6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6ab-103">Snapshot 개체에 대 한 키 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ab6ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab6ab-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab6ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ab6ab-106">**Set-AzSnapshotKeyEncryptionKey** cmdlet은 snapshot 개체에 대 한 키 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ab6ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ab6ab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab6ab-108">Example 1</span></span>
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

<span data-ttu-id="ab6ab-109">첫 번째 명령은 Standard_LRS 저장소 계정 형식의 크기가 5GB 인 로컬 빈 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ab6ab-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ab6ab-111">두 번째 및 세 번째 명령은 snapshot 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="ab6ab-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ab6ab-113">변수</span><span class="sxs-lookup"><span data-stu-id="ab6ab-113">PARAMETERS</span></span>

### <span data-ttu-id="ab6ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6ab-114">-DefaultProfile</span></span>
<span data-ttu-id="ab6ab-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab6ab-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="ab6ab-116">-KeyUrl</span></span>
<span data-ttu-id="ab6ab-117">키 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="ab6ab-118">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="ab6ab-118">-Snapshot</span></span>
<span data-ttu-id="ab6ab-119">로컬 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab6ab-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ab6ab-120">-SourceVaultId</span></span>
<span data-ttu-id="ab6ab-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ab6ab-122">-확인</span><span class="sxs-lookup"><span data-stu-id="ab6ab-122">-Confirm</span></span>
<span data-ttu-id="ab6ab-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab6ab-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab6ab-124">-WhatIf</span></span>
<span data-ttu-id="ab6ab-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab6ab-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab6ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6ab-127">CommonParameters</span></span>
<span data-ttu-id="ab6ab-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6ab-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab6ab-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6ab-130">입력</span><span class="sxs-lookup"><span data-stu-id="ab6ab-130">INPUTS</span></span>

### <span data-ttu-id="ab6ab-131">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ab6ab-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="ab6ab-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab6ab-132">System.String</span></span>

## <span data-ttu-id="ab6ab-133">출력</span><span class="sxs-lookup"><span data-stu-id="ab6ab-133">OUTPUTS</span></span>

### <span data-ttu-id="ab6ab-134">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ab6ab-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ab6ab-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ab6ab-135">NOTES</span></span>

## <span data-ttu-id="ab6ab-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab6ab-136">RELATED LINKS</span></span>
