---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 12e84ee5456acc0c56eed0f35b0bf3c23813b31f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527595"
---
# <span data-ttu-id="0712c-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0712c-101">Set-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="0712c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0712c-102">SYNOPSIS</span></span>
<span data-ttu-id="0712c-103">지정 된 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0712c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0712c-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0712c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0712c-105">DESCRIPTION</span></span>
<span data-ttu-id="0712c-106">**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-106">The **Set-AzureRmDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="0712c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0712c-107">EXAMPLES</span></span>

### <span data-ttu-id="0712c-108">예제 1: 신뢰할 수 있는 Id 공급자 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="0712c-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="0712c-109">이는 "ContosoADL" 계정에서 "MyProvider" 방화벽 규칙에 대 한 공급자 endpoing을 "" "로 업데이트 합니다. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="0712c-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="0712c-110">변수</span><span class="sxs-lookup"><span data-stu-id="0712c-110">PARAMETERS</span></span>

### <span data-ttu-id="0712c-111">-계정</span><span class="sxs-lookup"><span data-stu-id="0712c-111">-Account</span></span>
<span data-ttu-id="0712c-112">신뢰할 수 있는 id 공급자를 추가 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="0712c-112">The Data Lake Store account to add the trusted identity provider to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0712c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0712c-113">-Name</span></span>
<span data-ttu-id="0712c-114">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="0712c-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="0712c-115">-ProviderEndpoint</span></span>
<span data-ttu-id="0712c-116">다음 형식의 유효한 신뢰할 수 있는 공급자 끝점입니다. https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="0712c-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="0712c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0712c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0712c-118">신뢰할 수 있는 id 공급자를 업데이트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-118">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="0712c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0712c-119">-Confirm</span></span>
<span data-ttu-id="0712c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0712c-121">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0712c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0712c-122">-DefaultProfile</span></span>
<span data-ttu-id="0712c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0712c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0712c-124">CommonParameters</span></span>
<span data-ttu-id="0712c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0712c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0712c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0712c-127">입력</span><span class="sxs-lookup"><span data-stu-id="0712c-127">INPUTS</span></span>

## <span data-ttu-id="0712c-128">출력</span><span class="sxs-lookup"><span data-stu-id="0712c-128">OUTPUTS</span></span>

### <span data-ttu-id="0712c-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="0712c-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="0712c-130">업데이트 된 신뢰할 수 있는 id 공급자입니다.</span><span class="sxs-lookup"><span data-stu-id="0712c-130">The updated trusted identity provider.</span></span>

## <span data-ttu-id="0712c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0712c-131">NOTES</span></span>

## <span data-ttu-id="0712c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0712c-132">RELATED LINKS</span></span>

