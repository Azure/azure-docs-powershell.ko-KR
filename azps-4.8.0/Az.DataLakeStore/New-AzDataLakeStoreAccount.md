---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212315"
---
# <span data-ttu-id="8019f-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8019f-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="8019f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8019f-102">SYNOPSIS</span></span>
<span data-ttu-id="8019f-103">새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="8019f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8019f-104">SYNTAX</span></span>

### <span data-ttu-id="8019f-105">UserOrSystemAssignedEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="8019f-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8019f-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="8019f-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8019f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8019f-107">DESCRIPTION</span></span>
<span data-ttu-id="8019f-108">**새 AzDataLakeStoreAccount** cmdlet은 새 Data Lake store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="8019f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8019f-109">EXAMPLES</span></span>

### <span data-ttu-id="8019f-110">예제 1: 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="8019f-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="8019f-111">이 명령은 미국 US 2 위치에 대해 ContosoADL 라는 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="8019f-112">변수</span><span class="sxs-lookup"><span data-stu-id="8019f-112">PARAMETERS</span></span>

### <span data-ttu-id="8019f-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="8019f-113">-DefaultGroup</span></span>
<span data-ttu-id="8019f-114">새 파일 및 폴더에 대 한 기본 그룹 소유자로 사용할 AzureActive Directory 그룹의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="8019f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8019f-115">-DefaultProfile</span></span>
<span data-ttu-id="8019f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8019f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8019f-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="8019f-117">-DisableEncryption</span></span>
<span data-ttu-id="8019f-118">계정에 암호화 된 형식이 적용 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8019f-119">-암호화</span><span class="sxs-lookup"><span data-stu-id="8019f-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8019f-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8019f-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8019f-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8019f-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8019f-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8019f-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8019f-123">-위치</span><span class="sxs-lookup"><span data-stu-id="8019f-123">-Location</span></span>
<span data-ttu-id="8019f-124">계정에 사용할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="8019f-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8019f-126">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="8019f-126">East US 2</span></span>

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

### <span data-ttu-id="8019f-127">-이름</span><span class="sxs-lookup"><span data-stu-id="8019f-127">-Name</span></span>
<span data-ttu-id="8019f-128">만들 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="8019f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8019f-129">-ResourceGroupName</span></span>
<span data-ttu-id="8019f-130">계정을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="8019f-131">태그</span><span class="sxs-lookup"><span data-stu-id="8019f-131">-Tag</span></span>
<span data-ttu-id="8019f-132">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="8019f-133">태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="8019f-134">-티어</span><span class="sxs-lookup"><span data-stu-id="8019f-134">-Tier</span></span>
<span data-ttu-id="8019f-135">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="8019f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8019f-136">CommonParameters</span></span>
<span data-ttu-id="8019f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8019f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8019f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8019f-139">입력</span><span class="sxs-lookup"><span data-stu-id="8019f-139">INPUTS</span></span>

### <span data-ttu-id="8019f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8019f-140">System.String</span></span>

### <span data-ttu-id="8019f-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8019f-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8019f-142">시스템 Null 허용 ' 1 [[DataLake Configtype, Microsoft DataLake. 31bf3856ad364e35, Version = 2.0.0.0, Culture = 중립, PublicKeyToken =],  점</span><span class="sxs-lookup"><span data-stu-id="8019f-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8019f-143">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8019f-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8019f-144">시스템 Null 허용 ' 1 [[DataLake]. TierType, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.</span><span class="sxs-lookup"><span data-stu-id="8019f-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8019f-145">출력</span><span class="sxs-lookup"><span data-stu-id="8019f-145">OUTPUTS</span></span>

### <span data-ttu-id="8019f-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8019f-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="8019f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8019f-147">NOTES</span></span>

## <span data-ttu-id="8019f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8019f-148">RELATED LINKS</span></span>

[<span data-ttu-id="8019f-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8019f-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="8019f-150">제거-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8019f-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="8019f-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8019f-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="8019f-152">테스트-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8019f-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


