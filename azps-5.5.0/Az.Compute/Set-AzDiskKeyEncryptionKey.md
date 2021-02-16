---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 6f2037b638b8fd055ef79ca6a8502a17bd5f7911
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199201"
---
# <span data-ttu-id="e395c-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e395c-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="e395c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e395c-102">SYNOPSIS</span></span>
<span data-ttu-id="e395c-103">디스크 개체에 대한 키 암호화 키 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="e395c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e395c-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e395c-105">설명</span><span class="sxs-lookup"><span data-stu-id="e395c-105">DESCRIPTION</span></span>
<span data-ttu-id="e395c-106">**Set-AzDiskKeyEncryptionKey** cmdlet은 디스크 개체에 대한 키 암호화 키 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="e395c-107">예제</span><span class="sxs-lookup"><span data-stu-id="e395c-107">EXAMPLES</span></span>

### <span data-ttu-id="e395c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e395c-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e395c-109">첫 번째 명령은 저장소 계정 유형에 크기가 5GB인 로컬 빈 Standard_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e395c-110">또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e395c-111">두 번째 및 세 번째 명령은 디스크 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="e395c-112">마지막 명령은 디스크 개체를 사용하며 리소스 그룹 'ResourceGroup01'에 'Disk01'으로 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e395c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e395c-113">PARAMETERS</span></span>

### <span data-ttu-id="e395c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e395c-114">-DefaultProfile</span></span>
<span data-ttu-id="e395c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e395c-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="e395c-116">-Disk</span></span>
<span data-ttu-id="e395c-117">로컬 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e395c-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="e395c-118">-KeyUrl</span></span>
<span data-ttu-id="e395c-119">키 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="e395c-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e395c-120">-SourceVaultId</span></span>
<span data-ttu-id="e395c-121">원본 자격 증명 모음 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="e395c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e395c-122">-Confirm</span></span>
<span data-ttu-id="e395c-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e395c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e395c-124">-WhatIf</span></span>
<span data-ttu-id="e395c-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e395c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e395c-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e395c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e395c-127">CommonParameters</span></span>
<span data-ttu-id="e395c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e395c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e395c-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e395c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e395c-130">입력</span><span class="sxs-lookup"><span data-stu-id="e395c-130">INPUTS</span></span>

### <span data-ttu-id="e395c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e395c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="e395c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e395c-132">System.String</span></span>

## <span data-ttu-id="e395c-133">출력</span><span class="sxs-lookup"><span data-stu-id="e395c-133">OUTPUTS</span></span>

### <span data-ttu-id="e395c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e395c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e395c-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e395c-135">NOTES</span></span>

## <span data-ttu-id="e395c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e395c-136">RELATED LINKS</span></span>
