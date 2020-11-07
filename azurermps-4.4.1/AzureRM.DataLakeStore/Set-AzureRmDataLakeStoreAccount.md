---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f9ebe1a541baf46e831dbe95b54b2881a03e7454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703382"
---
# <span data-ttu-id="04382-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="04382-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="04382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04382-102">SYNOPSIS</span></span>
<span data-ttu-id="04382-103">Data Lake Store 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04382-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04382-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tags] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04382-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04382-105">DESCRIPTION</span></span>
<span data-ttu-id="04382-106">**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="04382-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04382-107">EXAMPLES</span></span>

### <span data-ttu-id="04382-108">예제 1: 계정에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="04382-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="04382-109">이 명령은 ContosoADL 이라는 Data Lake Store 계정에 지정 된 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="04382-110">변수</span><span class="sxs-lookup"><span data-stu-id="04382-110">PARAMETERS</span></span>

### <span data-ttu-id="04382-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="04382-111">-AllowAzureIpState</span></span>
<span data-ttu-id="04382-112">방화벽을 통해 Azure 시작 Ip를 선택적으로 허용/차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="04382-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="04382-113">-DefaultGroup</span></span>
<span data-ttu-id="04382-114">AzureActive Directory 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="04382-115">이 그룹은 사용자가 만든 파일 및 폴더의 기본 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="04382-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="04382-116">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="04382-116">-FirewallState</span></span>
<span data-ttu-id="04382-117">선택적으로 기존 방화벽 규칙을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-117">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="04382-118">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="04382-118">-KeyVersion</span></span>
<span data-ttu-id="04382-119">암호화 유형이 사용자 지정 인 경우 사용자는이 매개 변수를 사용 하 여 해당 키 버전을 회전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04382-119">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="04382-120">-이름</span><span class="sxs-lookup"><span data-stu-id="04382-120">-Name</span></span>
<span data-ttu-id="04382-121">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-121">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="04382-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04382-122">-ResourceGroupName</span></span>
<span data-ttu-id="04382-123">수정할 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-123">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="04382-124">태그</span><span class="sxs-lookup"><span data-stu-id="04382-124">-Tags</span></span>
<span data-ttu-id="04382-125">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-125">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="04382-126">태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04382-126">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="04382-127">-티어</span><span class="sxs-lookup"><span data-stu-id="04382-127">-Tier</span></span>
<span data-ttu-id="04382-128">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="04382-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="04382-129">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="04382-129">-TrustedIdProviderState</span></span>
<span data-ttu-id="04382-130">필요에 따라 기존 신뢰할 수 있는 ID 공급자를 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-130">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="04382-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04382-131">-DefaultProfile</span></span>
<span data-ttu-id="04382-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04382-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04382-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04382-133">CommonParameters</span></span>
<span data-ttu-id="04382-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04382-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04382-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04382-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04382-136">입력</span><span class="sxs-lookup"><span data-stu-id="04382-136">INPUTS</span></span>

## <span data-ttu-id="04382-137">출력</span><span class="sxs-lookup"><span data-stu-id="04382-137">OUTPUTS</span></span>

### <span data-ttu-id="04382-138">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="04382-138">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="04382-139">업데이트 된 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="04382-139">The updated account details.</span></span>

## <span data-ttu-id="04382-140">상속자</span><span class="sxs-lookup"><span data-stu-id="04382-140">NOTES</span></span>

## <span data-ttu-id="04382-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04382-141">RELATED LINKS</span></span>

[<span data-ttu-id="04382-142">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="04382-142">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="04382-143">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="04382-143">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="04382-144">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="04382-144">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="04382-145">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="04382-145">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


