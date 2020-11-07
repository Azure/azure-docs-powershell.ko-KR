---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711901"
---
# <span data-ttu-id="4c41d-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4c41d-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="4c41d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c41d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c41d-103">새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c41d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c41d-104">SYNTAX</span></span>

### <span data-ttu-id="4c41d-105">사용자 또는 시스템 암호화가 지정 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4c41d-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c41d-106">암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="4c41d-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c41d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4c41d-107">DESCRIPTION</span></span>
<span data-ttu-id="4c41d-108">**새 AzureRmDataLakeStoreAccount** cmdlet은 새 Data Lake store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="4c41d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4c41d-109">EXAMPLES</span></span>

### <span data-ttu-id="4c41d-110">예제 1: 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="4c41d-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="4c41d-111">이 명령은 미국 US 2 위치에 대해 ContosoADL 라는 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="4c41d-112">변수</span><span class="sxs-lookup"><span data-stu-id="4c41d-112">PARAMETERS</span></span>

### <span data-ttu-id="4c41d-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="4c41d-113">-DefaultGroup</span></span>
<span data-ttu-id="4c41d-114">새 파일 및 폴더에 대 한 기본 그룹 소유자로 사용할 AzureActive Directory 그룹의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="4c41d-115">-DisableEncryption</span></span>
<span data-ttu-id="4c41d-116">계정에 암호화 된 형식이 적용 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-117">-암호화</span><span class="sxs-lookup"><span data-stu-id="4c41d-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4c41d-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-119">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4c41d-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="4c41d-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-121">-위치</span><span class="sxs-lookup"><span data-stu-id="4c41d-121">-Location</span></span>
<span data-ttu-id="4c41d-122">계정에 사용할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="4c41d-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c41d-124">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="4c41d-124">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4c41d-125">-Name</span></span>
<span data-ttu-id="4c41d-126">만들 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-126">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="4c41d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c41d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4c41d-128">계정을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-128">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-129">태그</span><span class="sxs-lookup"><span data-stu-id="4c41d-129">-Tags</span></span>
<span data-ttu-id="4c41d-130">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="4c41d-131">태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-132">-티어</span><span class="sxs-lookup"><span data-stu-id="4c41d-132">-Tier</span></span>
<span data-ttu-id="4c41d-133">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-133">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c41d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c41d-134">-DefaultProfile</span></span>
<span data-ttu-id="4c41d-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c41d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c41d-136">CommonParameters</span></span>
<span data-ttu-id="4c41d-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c41d-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c41d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c41d-139">입력</span><span class="sxs-lookup"><span data-stu-id="4c41d-139">INPUTS</span></span>

## <span data-ttu-id="4c41d-140">출력</span><span class="sxs-lookup"><span data-stu-id="4c41d-140">OUTPUTS</span></span>

### <span data-ttu-id="4c41d-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4c41d-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="4c41d-142">만든 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="4c41d-142">The created account details.</span></span>

## <span data-ttu-id="4c41d-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4c41d-143">NOTES</span></span>

## <span data-ttu-id="4c41d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c41d-144">RELATED LINKS</span></span>

[<span data-ttu-id="4c41d-145">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4c41d-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4c41d-146">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4c41d-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4c41d-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4c41d-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4c41d-148">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4c41d-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


