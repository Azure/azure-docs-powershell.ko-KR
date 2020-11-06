---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 22eac04b24e8fec1778578f4e54792b5dcde6d1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536808"
---
# <span data-ttu-id="ff554-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff554-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="ff554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff554-102">SYNOPSIS</span></span>
<span data-ttu-id="ff554-103">Data Lake Store 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff554-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff554-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff554-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ff554-105">DESCRIPTION</span></span>
<span data-ttu-id="ff554-106">**AzureRmDataLakeStoreAccount** Cmdlet은 Data Lake store 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="ff554-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ff554-107">EXAMPLES</span></span>

### <span data-ttu-id="ff554-108">예제 1: 계정에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="ff554-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="ff554-109">이 명령은 ContosoADL 이라는 Data Lake Store 계정에 지정 된 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="ff554-110">변수</span><span class="sxs-lookup"><span data-stu-id="ff554-110">PARAMETERS</span></span>

### <span data-ttu-id="ff554-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="ff554-111">-AllowAzureIpState</span></span>
<span data-ttu-id="ff554-112">방화벽을 통해 Azure 시작 Ip를 선택적으로 허용/차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff554-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="ff554-113">-DefaultGroup</span></span>
<span data-ttu-id="ff554-114">AzureActive Directory 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="ff554-115">이 그룹은 사용자가 만든 파일 및 폴더의 기본 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff554-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff554-116">-DefaultProfile</span></span>
<span data-ttu-id="ff554-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff554-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff554-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="ff554-118">-FirewallState</span></span>
<span data-ttu-id="ff554-119">선택적으로 기존 방화벽 규칙을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff554-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ff554-120">-KeyVersion</span></span>
<span data-ttu-id="ff554-121">암호화 유형이 사용자 지정 인 경우 사용자는이 매개 변수를 사용 하 여 해당 키 버전을 회전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff554-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ff554-122">-Name</span></span>
<span data-ttu-id="ff554-123">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="ff554-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff554-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff554-125">수정할 Data Lake Store 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="ff554-126">태그</span><span class="sxs-lookup"><span data-stu-id="ff554-126">-Tag</span></span>
<span data-ttu-id="ff554-127">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ff554-128">태그를 사용 하 여 다른 Azure 리소스에서 Data Lake Store 계정을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff554-129">-티어</span><span class="sxs-lookup"><span data-stu-id="ff554-129">-Tier</span></span>
<span data-ttu-id="ff554-130">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="ff554-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="ff554-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="ff554-132">필요에 따라 기존 신뢰할 수 있는 ID 공급자를 설정 하거나 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: TrustedIdProviderState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff554-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff554-133">CommonParameters</span></span>
<span data-ttu-id="ff554-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff554-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff554-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff554-136">입력</span><span class="sxs-lookup"><span data-stu-id="ff554-136">INPUTS</span></span>

### <span data-ttu-id="ff554-137">않아야</span><span class="sxs-lookup"><span data-stu-id="ff554-137">None</span></span>
<span data-ttu-id="ff554-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff554-139">출력</span><span class="sxs-lookup"><span data-stu-id="ff554-139">OUTPUTS</span></span>

### <span data-ttu-id="ff554-140">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff554-140">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="ff554-141">업데이트 된 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="ff554-141">The updated account details.</span></span>

## <span data-ttu-id="ff554-142">상속자</span><span class="sxs-lookup"><span data-stu-id="ff554-142">NOTES</span></span>

## <span data-ttu-id="ff554-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff554-143">RELATED LINKS</span></span>

[<span data-ttu-id="ff554-144">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff554-144">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ff554-145">새로운 AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff554-145">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ff554-146">제거-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff554-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ff554-147">테스트-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff554-147">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


