---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868502"
---
# <span data-ttu-id="ee1b7-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ee1b7-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="ee1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1b7-103">Data Lake Store 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="ee1b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee1b7-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee1b7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee1b7-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1b7-106">**AzDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="ee1b7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee1b7-107">EXAMPLES</span></span>

### <span data-ttu-id="ee1b7-108">예제 1: 계정에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="ee1b7-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="ee1b7-109">이 명령은 ContosoADL 이라는 Data Lake Store 계정에 지정 된 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="ee1b7-110">변수</span><span class="sxs-lookup"><span data-stu-id="ee1b7-110">PARAMETERS</span></span>

### <span data-ttu-id="ee1b7-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="ee1b7-111">-AllowAzureIpState</span></span>
<span data-ttu-id="ee1b7-112">방화벽을 통해 Azure 시작 Ip를 선택적으로 허용/차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b7-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="ee1b7-113">-DefaultGroup</span></span>
<span data-ttu-id="ee1b7-114">AzureActive Directory 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="ee1b7-115">이 그룹은 사용자가 만든 파일 및 폴더의 기본 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="ee1b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1b7-116">-DefaultProfile</span></span>
<span data-ttu-id="ee1b7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ee1b7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee1b7-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="ee1b7-118">-FirewallState</span></span>
<span data-ttu-id="ee1b7-119">선택적으로 기존 방화벽 규칙을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b7-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ee1b7-120">-KeyVersion</span></span>
<span data-ttu-id="ee1b7-121">암호화 유형이 사용자 지정 인 경우 사용자는이 매개 변수를 사용 하 여 해당 키 버전을 회전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ee1b7-122">-Name</span></span>
<span data-ttu-id="ee1b7-123">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="ee1b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee1b7-125">수정할 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="ee1b7-126">태그</span><span class="sxs-lookup"><span data-stu-id="ee1b7-126">-Tag</span></span>
<span data-ttu-id="ee1b7-127">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ee1b7-128">태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b7-129">-티어</span><span class="sxs-lookup"><span data-stu-id="ee1b7-129">-Tier</span></span>
<span data-ttu-id="ee1b7-130">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ee1b7-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="ee1b7-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="ee1b7-132">필요에 따라 기존 신뢰할 수 있는 ID 공급자를 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1b7-133">CommonParameters</span></span>
<span data-ttu-id="ee1b7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1b7-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1b7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1b7-136">입력</span><span class="sxs-lookup"><span data-stu-id="ee1b7-136">INPUTS</span></span>

### <span data-ttu-id="ee1b7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee1b7-137">System.String</span></span>

### <span data-ttu-id="ee1b7-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ee1b7-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ee1b7-139">시스템 Null 허용 ' 1 [[DataLake]. TrustedIdProviderState, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ee1b7-140">시스템 Null 허용 ' 1 [[DataLake]. FirewallState, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ee1b7-141">시스템 Null 허용 ' 1 [[DataLake]. TierType, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ee1b7-142">시스템 Null 허용 ' 1 [[DataLake]. FirewallAllowAzureIpsState, DataLake, Version = 2.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]],.</span><span class="sxs-lookup"><span data-stu-id="ee1b7-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ee1b7-143">출력</span><span class="sxs-lookup"><span data-stu-id="ee1b7-143">OUTPUTS</span></span>

### <span data-ttu-id="ee1b7-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ee1b7-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="ee1b7-145">상속자</span><span class="sxs-lookup"><span data-stu-id="ee1b7-145">NOTES</span></span>

## <span data-ttu-id="ee1b7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee1b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="ee1b7-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ee1b7-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ee1b7-148">새로운 AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ee1b7-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ee1b7-149">제거-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ee1b7-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ee1b7-150">테스트-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ee1b7-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


