---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349322"
---
# <span data-ttu-id="607cd-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="607cd-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="607cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607cd-102">SYNOPSIS</span></span>
<span data-ttu-id="607cd-103">스냅숏 업데이트 개체에서 디스크 암호화 키 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="607cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="607cd-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="607cd-105">설명</span><span class="sxs-lookup"><span data-stu-id="607cd-105">DESCRIPTION</span></span>
<span data-ttu-id="607cd-106">**Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet은 스냅숏 업데이트 개체의 디스크 암호화 키 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="607cd-107">예제</span><span class="sxs-lookup"><span data-stu-id="607cd-107">EXAMPLES</span></span>

### <span data-ttu-id="607cd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="607cd-108">Example 1</span></span>
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

<span data-ttu-id="607cd-109">첫 번째 명령은 저장소 계정 유형에서 크기가 10GB인 로컬 빈 스냅숏 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="607cd-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="607cd-111">두 번째 및 세 번째 명령은 스냅숏 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="607cd-112">마지막 명령은 스냅숏 업데이트 개체를 생성하고 리소스 그룹 'ResourceGroup01'에서 'Snapshot01'으로 기존 스냅숏을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="607cd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607cd-113">PARAMETERS</span></span>

### <span data-ttu-id="607cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607cd-114">-DefaultProfile</span></span>
<span data-ttu-id="607cd-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="607cd-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="607cd-116">-SecretUrl</span></span>
<span data-ttu-id="607cd-117">비밀 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="607cd-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="607cd-118">-SnapshotUpdate</span></span>
<span data-ttu-id="607cd-119">로컬 스냅숏 업데이트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="607cd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="607cd-120">-SourceVaultId</span></span>
<span data-ttu-id="607cd-121">원본 자격 증명 모음 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="607cd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="607cd-122">-Confirm</span></span>
<span data-ttu-id="607cd-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="607cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607cd-124">-WhatIf</span></span>
<span data-ttu-id="607cd-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="607cd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607cd-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="607cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607cd-127">CommonParameters</span></span>
<span data-ttu-id="607cd-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="607cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607cd-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="607cd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607cd-130">입력</span><span class="sxs-lookup"><span data-stu-id="607cd-130">INPUTS</span></span>

### <span data-ttu-id="607cd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="607cd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="607cd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="607cd-132">System.String</span></span>

## <span data-ttu-id="607cd-133">출력</span><span class="sxs-lookup"><span data-stu-id="607cd-133">OUTPUTS</span></span>

### <span data-ttu-id="607cd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="607cd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="607cd-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="607cd-135">NOTES</span></span>

## <span data-ttu-id="607cd-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="607cd-136">RELATED LINKS</span></span>
