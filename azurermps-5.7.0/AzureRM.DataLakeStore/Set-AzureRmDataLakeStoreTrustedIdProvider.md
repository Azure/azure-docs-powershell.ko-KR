---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 29f9bbab5d3f7590d53bc405d80ea9e5c484fd5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531063"
---
# <span data-ttu-id="8b970-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8b970-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8b970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b970-102">SYNOPSIS</span></span>
<span data-ttu-id="8b970-103">지정 된 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b970-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b970-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b970-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b970-105">DESCRIPTION</span></span>
<span data-ttu-id="8b970-106">**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8b970-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b970-107">EXAMPLES</span></span>

### <span data-ttu-id="8b970-108">예제 1: 신뢰할 수 있는 Id 공급자 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="8b970-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="8b970-109">이는 "ContosoADL" 계정에서 "MyProvider" 방화벽 규칙에 대 한 공급자 endpoing을 "" "로 업데이트 합니다. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="8b970-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="8b970-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b970-110">PARAMETERS</span></span>

### <span data-ttu-id="8b970-111">-계정</span><span class="sxs-lookup"><span data-stu-id="8b970-111">-Account</span></span>
<span data-ttu-id="8b970-112">신뢰할 수 있는 id 공급자를 추가 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="8b970-112">The Data Lake Store account to add the trusted identity provider to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b970-113">-DefaultProfile</span></span>
<span data-ttu-id="8b970-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8b970-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b970-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8b970-115">-Name</span></span>
<span data-ttu-id="8b970-116">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="8b970-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b970-117">-ProviderEndpoint</span></span>
<span data-ttu-id="8b970-118">다음 형식의 유효한 신뢰할 수 있는 공급자 끝점입니다. https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="8b970-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="8b970-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b970-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b970-120">신뢰할 수 있는 id 공급자를 업데이트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="8b970-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8b970-121">-Confirm</span></span>
<span data-ttu-id="8b970-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b970-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b970-123">-WhatIf</span></span>
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

### <span data-ttu-id="8b970-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b970-124">CommonParameters</span></span>
<span data-ttu-id="8b970-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b970-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b970-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b970-127">입력</span><span class="sxs-lookup"><span data-stu-id="8b970-127">INPUTS</span></span>

### <span data-ttu-id="8b970-128">않아야</span><span class="sxs-lookup"><span data-stu-id="8b970-128">None</span></span>
<span data-ttu-id="8b970-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b970-130">출력</span><span class="sxs-lookup"><span data-stu-id="8b970-130">OUTPUTS</span></span>

### <span data-ttu-id="8b970-131">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8b970-131">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="8b970-132">업데이트 된 신뢰할 수 있는 id 공급자입니다.</span><span class="sxs-lookup"><span data-stu-id="8b970-132">The updated trusted identity provider.</span></span>

## <span data-ttu-id="8b970-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8b970-133">NOTES</span></span>

## <span data-ttu-id="8b970-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b970-134">RELATED LINKS</span></span>

