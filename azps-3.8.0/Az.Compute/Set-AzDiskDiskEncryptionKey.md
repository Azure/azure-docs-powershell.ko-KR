---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 53a8ef8455fe95647b7b51473828f7684495aab7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045049"
---
# <span data-ttu-id="8dcee-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8dcee-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="8dcee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dcee-102">SYNOPSIS</span></span>
<span data-ttu-id="8dcee-103">디스크 개체의 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="8dcee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dcee-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dcee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8dcee-105">DESCRIPTION</span></span>
<span data-ttu-id="8dcee-106">**Set-AzDiskDiskEncryptionKey** cmdlet은 디스크 개체의 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="8dcee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8dcee-107">EXAMPLES</span></span>

### <span data-ttu-id="8dcee-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dcee-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1'; 
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="8dcee-109">첫 번째 명령은 Standard_LRS 저장소 계정 유형의 크기가 5GB 인 로컬 빈 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="8dcee-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8dcee-111">두 번째 및 세 번째 명령은 disk 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="8dcee-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8dcee-113">변수</span><span class="sxs-lookup"><span data-stu-id="8dcee-113">PARAMETERS</span></span>

### <span data-ttu-id="8dcee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dcee-114">-DefaultProfile</span></span>
<span data-ttu-id="8dcee-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dcee-116">-디스크</span><span class="sxs-lookup"><span data-stu-id="8dcee-116">-Disk</span></span>
<span data-ttu-id="8dcee-117">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="8dcee-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="8dcee-118">-SecretUrl</span></span>
<span data-ttu-id="8dcee-119">비밀 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="8dcee-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="8dcee-120">-SourceVaultId</span></span>
<span data-ttu-id="8dcee-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="8dcee-122">-확인</span><span class="sxs-lookup"><span data-stu-id="8dcee-122">-Confirm</span></span>
<span data-ttu-id="8dcee-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dcee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dcee-124">-WhatIf</span></span>
<span data-ttu-id="8dcee-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dcee-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dcee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dcee-127">CommonParameters</span></span>
<span data-ttu-id="8dcee-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dcee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dcee-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8dcee-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dcee-130">입력</span><span class="sxs-lookup"><span data-stu-id="8dcee-130">INPUTS</span></span>

### <span data-ttu-id="8dcee-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="8dcee-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="8dcee-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8dcee-132">System.String</span></span>

## <span data-ttu-id="8dcee-133">출력</span><span class="sxs-lookup"><span data-stu-id="8dcee-133">OUTPUTS</span></span>

### <span data-ttu-id="8dcee-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="8dcee-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="8dcee-135">상속자</span><span class="sxs-lookup"><span data-stu-id="8dcee-135">NOTES</span></span>

## <span data-ttu-id="8dcee-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dcee-136">RELATED LINKS</span></span>
