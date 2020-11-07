---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 6a1994979cc6521cee083b07f336a76a54dd7cb7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881885"
---
# <span data-ttu-id="413a9-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="413a9-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="413a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="413a9-102">SYNOPSIS</span></span>
<span data-ttu-id="413a9-103">키 보관소 관리 저장소 SAS 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="413a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="413a9-104">SYNTAX</span></span>

### <span data-ttu-id="413a9-105">ByAccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="413a9-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="413a9-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="413a9-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413a9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="413a9-107">DESCRIPTION</span></span>
<span data-ttu-id="413a9-108">정의 이름이 지정 된 경우 키 보관소 관리 저장소 SAS 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="413a9-109">정의 이름을 지정 하지 않으면 자격 증명 모음에 지정 된 키 보관소 관리 저장소 계정과 연결 된 모든 SAS 정의가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="413a9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="413a9-110">EXAMPLES</span></span>

### <span data-ttu-id="413a9-111">예제 1: 모든 키 자격 증명 모음 관리 저장소 SAS 정의 나열</span><span class="sxs-lookup"><span data-stu-id="413a9-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="413a9-112">키 자격 증명 모음 ' mystorageaccount '와 연결 된 모든 SAS 정의가 자격 증명 모음 ' myvault '에 의해 관리 됨</span><span class="sxs-lookup"><span data-stu-id="413a9-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="413a9-113">예제 2: 키 보관소 관리 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="413a9-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="413a9-114">자격 증명 모음 ' mystorageaccount '에 의해 관리 되는 키 보관소 관리 저장소 계정 ' mysasDef '에 연결 된 ' t e 볼트 '의 SAS 정의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="413a9-115">변수</span><span class="sxs-lookup"><span data-stu-id="413a9-115">PARAMETERS</span></span>

### <span data-ttu-id="413a9-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="413a9-116">-AccountName</span></span>
<span data-ttu-id="413a9-117">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="413a9-117">Vault name.</span></span>
<span data-ttu-id="413a9-118">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413a9-119">-DefaultProfile</span></span>
<span data-ttu-id="413a9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="413a9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="413a9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="413a9-121">-Name</span></span>
<span data-ttu-id="413a9-122">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-122">Storage sas definition name.</span></span>
<span data-ttu-id="413a9-123">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413a9-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="413a9-124">-VaultName</span></span>
<span data-ttu-id="413a9-125">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="413a9-125">Vault name.</span></span>
<span data-ttu-id="413a9-126">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413a9-127">CommonParameters</span></span>
<span data-ttu-id="413a9-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="413a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413a9-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413a9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413a9-130">입력</span><span class="sxs-lookup"><span data-stu-id="413a9-130">INPUTS</span></span>

### <span data-ttu-id="413a9-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="413a9-131">System.String</span></span>

## <span data-ttu-id="413a9-132">출력</span><span class="sxs-lookup"><span data-stu-id="413a9-132">OUTPUTS</span></span>

### <span data-ttu-id="413a9-133">System.webserver. List ' 1 [[Microsoft Azure. l t e.]. \* [[2.5.0.0]. \* [[$]. \*. \*, Microsoft Azure. 명령이. KeyVault, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="413a9-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="413a9-134">Microsoft. KeyVault. ' Managed' 모델. i 볼트로 Esasdefinition</span><span class="sxs-lookup"><span data-stu-id="413a9-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="413a9-135">상속자</span><span class="sxs-lookup"><span data-stu-id="413a9-135">NOTES</span></span>

## <span data-ttu-id="413a9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="413a9-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

