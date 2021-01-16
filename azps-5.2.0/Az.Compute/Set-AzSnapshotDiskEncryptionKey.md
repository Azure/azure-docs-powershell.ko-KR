---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325653"
---
# <span data-ttu-id="ea2e9-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ea2e9-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="ea2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2e9-103">스냅숏 개체에 대한 디스크 암호화 키 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ea2e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea2e9-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea2e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="ea2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2e9-106">**Set-AzSnapshotDiskEncryptionKey** cmdlet은 스냅숏 개체에 대한 디스크 암호화 키 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="ea2e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="ea2e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ea2e9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea2e9-108">Example 1</span></span>
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

<span data-ttu-id="ea2e9-109">첫 번째 명령은 저장소 계정 유형에서 크기가 5GB인 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ea2e9-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ea2e9-111">두 번째 및 세 번째 명령은 스냅숏 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="ea2e9-112">마지막 명령은 스냅숏 개체를 만들고 리소스 그룹 'ResourceGroup01'에서 'Snapshot01'으로 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ea2e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea2e9-113">PARAMETERS</span></span>

### <span data-ttu-id="ea2e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2e9-114">-DefaultProfile</span></span>
<span data-ttu-id="ea2e9-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea2e9-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="ea2e9-116">-SecretUrl</span></span>
<span data-ttu-id="ea2e9-117">비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="ea2e9-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="ea2e9-118">-Snapshot</span></span>
<span data-ttu-id="ea2e9-119">로컬 스냅숏 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="ea2e9-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ea2e9-120">-SourceVaultId</span></span>
<span data-ttu-id="ea2e9-121">원본 자격 증명 모음 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ea2e9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea2e9-122">-Confirm</span></span>
<span data-ttu-id="ea2e9-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea2e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2e9-124">-WhatIf</span></span>
<span data-ttu-id="ea2e9-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ea2e9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea2e9-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea2e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2e9-127">CommonParameters</span></span>
<span data-ttu-id="ea2e9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2e9-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea2e9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2e9-130">입력</span><span class="sxs-lookup"><span data-stu-id="ea2e9-130">INPUTS</span></span>

### <span data-ttu-id="ea2e9-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ea2e9-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="ea2e9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ea2e9-132">System.String</span></span>

## <span data-ttu-id="ea2e9-133">출력</span><span class="sxs-lookup"><span data-stu-id="ea2e9-133">OUTPUTS</span></span>

### <span data-ttu-id="ea2e9-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ea2e9-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ea2e9-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea2e9-135">NOTES</span></span>

## <span data-ttu-id="ea2e9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea2e9-136">RELATED LINKS</span></span>
