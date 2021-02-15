---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204352"
---
# <span data-ttu-id="b6294-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6294-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="b6294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6294-102">SYNOPSIS</span></span>
<span data-ttu-id="b6294-103">새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="b6294-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6294-104">SYNTAX</span></span>

### <span data-ttu-id="b6294-105">UserOrSystemAssignedEncryption(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6294-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6294-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="b6294-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6294-107">설명</span><span class="sxs-lookup"><span data-stu-id="b6294-107">DESCRIPTION</span></span>
<span data-ttu-id="b6294-108">**New-AzDataLakeStoreAccount** cmdlet은 새 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="b6294-109">예제</span><span class="sxs-lookup"><span data-stu-id="b6294-109">EXAMPLES</span></span>

### <span data-ttu-id="b6294-110">예제 1: 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="b6294-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="b6294-111">이 명령은 미국 동부 2 위치에 대해 ContosoADL이라는 Data Lake Store 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="b6294-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6294-112">PARAMETERS</span></span>

### <span data-ttu-id="b6294-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="b6294-113">-DefaultGroup</span></span>
<span data-ttu-id="b6294-114">새 파일 및 폴더의 기본 그룹 소유자로 사용할 AzureActive Directory 그룹의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="b6294-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6294-115">-DefaultProfile</span></span>
<span data-ttu-id="b6294-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6294-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6294-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="b6294-117">-DisableEncryption</span></span>
<span data-ttu-id="b6294-118">계정에 적용된 어떠한 형태의 암호화도 없는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="b6294-119">-Encryption</span><span class="sxs-lookup"><span data-stu-id="b6294-119">-Encryption</span></span>
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

### <span data-ttu-id="b6294-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b6294-120">-KeyName</span></span>
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

### <span data-ttu-id="b6294-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="b6294-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="b6294-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="b6294-122">-KeyVersion</span></span>
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

### <span data-ttu-id="b6294-123">-Location</span><span class="sxs-lookup"><span data-stu-id="b6294-123">-Location</span></span>
<span data-ttu-id="b6294-124">계정에 사용할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="b6294-125">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="b6294-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6294-126">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="b6294-126">East US 2</span></span>

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

### <span data-ttu-id="b6294-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b6294-127">-Name</span></span>
<span data-ttu-id="b6294-128">만들 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="b6294-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6294-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6294-130">계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="b6294-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6294-131">-Tag</span></span>
<span data-ttu-id="b6294-132">태그를 키-값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="b6294-133">태그를 사용하여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="b6294-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="b6294-134">-Tier</span></span>
<span data-ttu-id="b6294-135">이 계정에 사용할 원하는 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="b6294-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6294-136">CommonParameters</span></span>
<span data-ttu-id="b6294-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6294-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6294-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6294-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6294-139">입력</span><span class="sxs-lookup"><span data-stu-id="b6294-139">INPUTS</span></span>

### <span data-ttu-id="b6294-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b6294-140">System.String</span></span>

### <span data-ttu-id="b6294-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6294-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b6294-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6294-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b6294-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6294-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b6294-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6294-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b6294-145">출력</span><span class="sxs-lookup"><span data-stu-id="b6294-145">OUTPUTS</span></span>

### <span data-ttu-id="b6294-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6294-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="b6294-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6294-147">NOTES</span></span>

## <span data-ttu-id="b6294-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6294-148">RELATED LINKS</span></span>

[<span data-ttu-id="b6294-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6294-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6294-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6294-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6294-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6294-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6294-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6294-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


