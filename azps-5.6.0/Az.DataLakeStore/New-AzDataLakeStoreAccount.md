---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: ee172856bb5935f1a6da4d6dcce92054bd1001e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952656"
---
# <span data-ttu-id="ca775-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ca775-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="ca775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca775-102">SYNOPSIS</span></span>
<span data-ttu-id="ca775-103">새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="ca775-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca775-104">SYNTAX</span></span>

### <span data-ttu-id="ca775-105">UserOrSystemAssignedEncryption(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca775-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca775-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="ca775-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca775-107">설명</span><span class="sxs-lookup"><span data-stu-id="ca775-107">DESCRIPTION</span></span>
<span data-ttu-id="ca775-108">**New-AzDataLakeStoreAccount** cmdlet은 새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="ca775-109">예제</span><span class="sxs-lookup"><span data-stu-id="ca775-109">EXAMPLES</span></span>

### <span data-ttu-id="ca775-110">예제 1: 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="ca775-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="ca775-111">이 명령은 미국 동부 2 위치에 대해 ContosoADL이라는 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="ca775-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca775-112">PARAMETERS</span></span>

### <span data-ttu-id="ca775-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="ca775-113">-DefaultGroup</span></span>
<span data-ttu-id="ca775-114">새 파일 및 폴더의 기본 그룹 소유자로 사용할 AzureActive Directory 그룹의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="ca775-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca775-115">-DefaultProfile</span></span>
<span data-ttu-id="ca775-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ca775-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca775-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="ca775-117">-DisableEncryption</span></span>
<span data-ttu-id="ca775-118">계정에 암호화 형식이 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="ca775-119">-Encryption</span><span class="sxs-lookup"><span data-stu-id="ca775-119">-Encryption</span></span>
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

### <span data-ttu-id="ca775-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ca775-120">-KeyName</span></span>
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

### <span data-ttu-id="ca775-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ca775-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="ca775-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ca775-122">-KeyVersion</span></span>
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

### <span data-ttu-id="ca775-123">-Location</span><span class="sxs-lookup"><span data-stu-id="ca775-123">-Location</span></span>
<span data-ttu-id="ca775-124">계정에 사용할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="ca775-125">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca775-126">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="ca775-126">East US 2</span></span>

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

### <span data-ttu-id="ca775-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ca775-127">-Name</span></span>
<span data-ttu-id="ca775-128">만들 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="ca775-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca775-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca775-130">계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="ca775-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca775-131">-Tag</span></span>
<span data-ttu-id="ca775-132">태그를 키 값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ca775-133">태그를 사용하여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="ca775-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="ca775-134">-Tier</span></span>
<span data-ttu-id="ca775-135">이 계정에 사용할 원하는 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ca775-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca775-136">CommonParameters</span></span>
<span data-ttu-id="ca775-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca775-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca775-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca775-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca775-139">입력</span><span class="sxs-lookup"><span data-stu-id="ca775-139">INPUTS</span></span>

### <span data-ttu-id="ca775-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ca775-140">System.String</span></span>

### <span data-ttu-id="ca775-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca775-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ca775-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ca775-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ca775-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ca775-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ca775-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ca775-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ca775-145">출력</span><span class="sxs-lookup"><span data-stu-id="ca775-145">OUTPUTS</span></span>

### <span data-ttu-id="ca775-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ca775-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="ca775-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca775-147">NOTES</span></span>

## <span data-ttu-id="ca775-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca775-148">RELATED LINKS</span></span>

[<span data-ttu-id="ca775-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ca775-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ca775-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ca775-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ca775-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ca775-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ca775-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ca775-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


