---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 2cb1cad343f57f164529e3607c1ad0b1ec74df05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880758"
---
# <span data-ttu-id="2ea22-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2ea22-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="2ea22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea22-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea22-103">관리 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ea22-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ea22-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea22-106">**AzureRmDisk** cmdlet은 관리 되는 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="2ea22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ea22-107">EXAMPLES</span></span>

### <span data-ttu-id="2ea22-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ea22-108">Example 1</span></span>
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

<span data-ttu-id="2ea22-109">첫 번째 명령은 Standard_LRS 저장소 계정 유형의 크기가 5GB 인 로컬 빈 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="2ea22-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2ea22-111">두 번째 및 세 번째 명령은 disk 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="2ea22-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2ea22-113">변수</span><span class="sxs-lookup"><span data-stu-id="2ea22-113">PARAMETERS</span></span>

### <span data-ttu-id="2ea22-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ea22-114">-AsJob</span></span>
<span data-ttu-id="2ea22-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea22-116">-DefaultProfile</span></span>
<span data-ttu-id="2ea22-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea22-118">-디스크</span><span class="sxs-lookup"><span data-stu-id="2ea22-118">-Disk</span></span>
<span data-ttu-id="2ea22-119">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea22-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="2ea22-120">-DiskName</span></span>
<span data-ttu-id="2ea22-121">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-121">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea22-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea22-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ea22-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea22-124">-확인</span><span class="sxs-lookup"><span data-stu-id="2ea22-124">-Confirm</span></span>
<span data-ttu-id="2ea22-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea22-126">-WhatIf</span></span>
<span data-ttu-id="2ea22-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea22-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea22-129">CommonParameters</span></span>
<span data-ttu-id="2ea22-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ea22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea22-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea22-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea22-132">입력</span><span class="sxs-lookup"><span data-stu-id="2ea22-132">INPUTS</span></span>

### <span data-ttu-id="2ea22-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ea22-133">System.String</span></span>
<span data-ttu-id="2ea22-134">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="2ea22-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="2ea22-135">출력</span><span class="sxs-lookup"><span data-stu-id="2ea22-135">OUTPUTS</span></span>

### <span data-ttu-id="2ea22-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="2ea22-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2ea22-137">상속자</span><span class="sxs-lookup"><span data-stu-id="2ea22-137">NOTES</span></span>

## <span data-ttu-id="2ea22-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ea22-138">RELATED LINKS</span></span>

