---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c9964bfb6d9f701d88a16b8a227aec7c2018a217
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526847"
---
# <span data-ttu-id="71775-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71775-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="71775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71775-102">SYNOPSIS</span></span>
<span data-ttu-id="71775-103">새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71775-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71775-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71775-104">SYNTAX</span></span>

### <span data-ttu-id="71775-105">UserOrSystemAssignedEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="71775-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71775-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="71775-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71775-107">설명은</span><span class="sxs-lookup"><span data-stu-id="71775-107">DESCRIPTION</span></span>
<span data-ttu-id="71775-108">**새 AzureRmDataLakeStoreAccount** cmdlet은 새 Data Lake store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71775-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="71775-109">예제의</span><span class="sxs-lookup"><span data-stu-id="71775-109">EXAMPLES</span></span>

### <span data-ttu-id="71775-110">예제 1: 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="71775-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="71775-111">이 명령은 미국 US 2 위치에 대해 ContosoADL 라는 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71775-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="71775-112">변수</span><span class="sxs-lookup"><span data-stu-id="71775-112">PARAMETERS</span></span>

### <span data-ttu-id="71775-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="71775-113">-DefaultGroup</span></span>
<span data-ttu-id="71775-114">새 파일 및 폴더에 대 한 기본 그룹 소유자로 사용할 AzureActive Directory 그룹의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71775-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71775-115">-DefaultProfile</span></span>
<span data-ttu-id="71775-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="71775-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71775-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="71775-117">-DisableEncryption</span></span>
<span data-ttu-id="71775-118">계정에 암호화 된 형식이 적용 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71775-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-119">-암호화</span><span class="sxs-lookup"><span data-stu-id="71775-119">-Encryption</span></span>
```yaml
Type: EncryptionConfigType
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="71775-120">-KeyName</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="71775-121">-KeyVaultId</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="71775-122">-KeyVersion</span></span>
```yaml
Type: String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-123">-위치</span><span class="sxs-lookup"><span data-stu-id="71775-123">-Location</span></span>
<span data-ttu-id="71775-124">계정에 사용할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71775-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="71775-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="71775-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71775-126">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="71775-126">East US 2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-127">-이름</span><span class="sxs-lookup"><span data-stu-id="71775-127">-Name</span></span>
<span data-ttu-id="71775-128">만들 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71775-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="71775-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71775-129">-ResourceGroupName</span></span>
<span data-ttu-id="71775-130">계정을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71775-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="71775-131">태그</span><span class="sxs-lookup"><span data-stu-id="71775-131">-Tag</span></span>
<span data-ttu-id="71775-132">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71775-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="71775-133">태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71775-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-134">-티어</span><span class="sxs-lookup"><span data-stu-id="71775-134">-Tier</span></span>
<span data-ttu-id="71775-135">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="71775-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71775-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71775-136">CommonParameters</span></span>
<span data-ttu-id="71775-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71775-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71775-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71775-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71775-139">입력</span><span class="sxs-lookup"><span data-stu-id="71775-139">INPUTS</span></span>

### <span data-ttu-id="71775-140">않아야</span><span class="sxs-lookup"><span data-stu-id="71775-140">None</span></span>
<span data-ttu-id="71775-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71775-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71775-142">출력</span><span class="sxs-lookup"><span data-stu-id="71775-142">OUTPUTS</span></span>

### <span data-ttu-id="71775-143">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71775-143">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="71775-144">만든 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="71775-144">The created account details.</span></span>

## <span data-ttu-id="71775-145">상속자</span><span class="sxs-lookup"><span data-stu-id="71775-145">NOTES</span></span>

## <span data-ttu-id="71775-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71775-146">RELATED LINKS</span></span>

[<span data-ttu-id="71775-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71775-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="71775-148">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71775-148">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="71775-149">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71775-149">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="71775-150">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71775-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


