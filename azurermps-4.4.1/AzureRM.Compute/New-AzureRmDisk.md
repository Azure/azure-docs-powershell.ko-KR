---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 4392c1ccf19474e1a8f73c5bccca2c09f53cbea8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711779"
---
# <span data-ttu-id="3a06f-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3a06f-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="3a06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a06f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a06f-103">관리 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a06f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a06f-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a06f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3a06f-105">DESCRIPTION</span></span>
<span data-ttu-id="3a06f-106">**AzureRmDisk** cmdlet은 관리 되는 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="3a06f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3a06f-107">EXAMPLES</span></span>

### <span data-ttu-id="3a06f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a06f-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="3a06f-109">첫 번째 명령은 Standard_LRS 저장소 계정 유형의 크기가 5GB 인 로컬 빈 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="3a06f-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3a06f-111">두 번째 및 세 번째 명령은 disk 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="3a06f-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3a06f-113">변수</span><span class="sxs-lookup"><span data-stu-id="3a06f-113">PARAMETERS</span></span>

### <span data-ttu-id="3a06f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a06f-114">-DefaultProfile</span></span>
<span data-ttu-id="3a06f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a06f-116">-디스크</span><span class="sxs-lookup"><span data-stu-id="3a06f-116">-Disk</span></span>
<span data-ttu-id="3a06f-117">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a06f-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3a06f-118">-DiskName</span></span>
<span data-ttu-id="3a06f-119">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-119">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="3a06f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a06f-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a06f-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a06f-122">-확인</span><span class="sxs-lookup"><span data-stu-id="3a06f-122">-Confirm</span></span>
<span data-ttu-id="3a06f-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a06f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a06f-124">-WhatIf</span></span>
<span data-ttu-id="3a06f-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a06f-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a06f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a06f-127">CommonParameters</span></span>
<span data-ttu-id="3a06f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a06f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a06f-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a06f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a06f-130">입력</span><span class="sxs-lookup"><span data-stu-id="3a06f-130">INPUTS</span></span>

### <span data-ttu-id="3a06f-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a06f-131">System.String</span></span>
<span data-ttu-id="3a06f-132">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="3a06f-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="3a06f-133">출력</span><span class="sxs-lookup"><span data-stu-id="3a06f-133">OUTPUTS</span></span>

### <span data-ttu-id="3a06f-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="3a06f-134">System.Object</span></span>

## <span data-ttu-id="3a06f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="3a06f-135">NOTES</span></span>

## <span data-ttu-id="3a06f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a06f-136">RELATED LINKS</span></span>

