---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4d44bc014a3d38a89e6c9a6a6d755aa9353c052e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531744"
---
# <span data-ttu-id="e7808-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e7808-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="e7808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7808-102">SYNOPSIS</span></span>
<span data-ttu-id="e7808-103">디스크 업데이트 개체에서 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-103">Sets the disk encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7808-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7808-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateDiskEncryptionKey [-DiskUpdate] <DiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7808-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7808-105">DESCRIPTION</span></span>
<span data-ttu-id="e7808-106">**Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet은 디스크 업데이트 개체에서 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-106">The **Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="e7808-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7808-107">EXAMPLES</span></span>

### <span data-ttu-id="e7808-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7808-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="e7808-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e7808-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e7808-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="e7808-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e7808-113">변수</span><span class="sxs-lookup"><span data-stu-id="e7808-113">PARAMETERS</span></span>

### <span data-ttu-id="e7808-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e7808-114">-DiskUpdate</span></span>
<span data-ttu-id="e7808-115">로컬 디스크 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7808-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="e7808-116">-SecretUrl</span></span>
<span data-ttu-id="e7808-117">비밀 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="e7808-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e7808-118">-SourceVaultId</span></span>
<span data-ttu-id="e7808-119">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="e7808-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e7808-120">-Confirm</span></span>
<span data-ttu-id="e7808-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7808-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7808-122">-WhatIf</span></span>
<span data-ttu-id="e7808-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7808-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7808-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7808-125">CommonParameters</span></span>
<span data-ttu-id="e7808-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7808-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7808-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7808-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7808-128">입력</span><span class="sxs-lookup"><span data-stu-id="e7808-128">INPUTS</span></span>

### <span data-ttu-id="e7808-129">Microsoft. 관리. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e7808-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="e7808-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e7808-130">System.String</span></span>

## <span data-ttu-id="e7808-131">출력</span><span class="sxs-lookup"><span data-stu-id="e7808-131">OUTPUTS</span></span>

### <span data-ttu-id="e7808-132">Microsoft. 관리. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e7808-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="e7808-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e7808-133">NOTES</span></span>

## <span data-ttu-id="e7808-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7808-134">RELATED LINKS</span></span>

