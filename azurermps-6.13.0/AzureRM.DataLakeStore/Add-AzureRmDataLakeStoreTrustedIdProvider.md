---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: a8c3e560ed66be9ae72d9f33e73af268e9fd5f85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532028"
---
# <span data-ttu-id="1ef8a-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="1ef8a-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1ef8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ef8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef8a-103">신뢰할 수 있는 id 공급자를 지정 된 Data Lake Store 계정에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ef8a-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ef8a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ef8a-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef8a-106">**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store 계정에 신뢰할 수 있는 id 공급자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="1ef8a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1ef8a-107">EXAMPLES</span></span>

### <span data-ttu-id="1ef8a-108">예제 1: 신뢰할 수 있는 id 공급자 추가</span><span class="sxs-lookup"><span data-stu-id="1ef8a-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="1ef8a-109">"MyProvider" 공급자를 "ContosoADL" 계정에 공급자 끝점 ""으로 추가 합니다. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="1ef8a-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="1ef8a-110">변수</span><span class="sxs-lookup"><span data-stu-id="1ef8a-110">PARAMETERS</span></span>

### <span data-ttu-id="1ef8a-111">-계정</span><span class="sxs-lookup"><span data-stu-id="1ef8a-111">-Account</span></span>
<span data-ttu-id="1ef8a-112">지정 된 신뢰할 수 있는 id 공급자를 추가할 Data Lake Store 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="1ef8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef8a-113">-DefaultProfile</span></span>
<span data-ttu-id="1ef8a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1ef8a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ef8a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1ef8a-115">-Name</span></span>
<span data-ttu-id="1ef8a-116">추가할 신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="1ef8a-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ef8a-117">-ProviderEndpoint</span></span>
<span data-ttu-id="1ef8a-118">다음 형식의 유효한 신뢰할 수 있는 공급자 끝점: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="1ef8a-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="1ef8a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ef8a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ef8a-120">신뢰할 수 있는 id 공급자를 추가할 계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="1ef8a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="1ef8a-121">-Confirm</span></span>
<span data-ttu-id="1ef8a-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ef8a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ef8a-123">-WhatIf</span></span>
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

### <span data-ttu-id="1ef8a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef8a-124">CommonParameters</span></span>
<span data-ttu-id="1ef8a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef8a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef8a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef8a-127">입력</span><span class="sxs-lookup"><span data-stu-id="1ef8a-127">INPUTS</span></span>

### <span data-ttu-id="1ef8a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1ef8a-128">System.String</span></span>

## <span data-ttu-id="1ef8a-129">출력</span><span class="sxs-lookup"><span data-stu-id="1ef8a-129">OUTPUTS</span></span>

### <span data-ttu-id="1ef8a-130">DataLakeStore. DataLakeStoreTrustedIdProvider/.</span><span class="sxs-lookup"><span data-stu-id="1ef8a-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="1ef8a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1ef8a-131">NOTES</span></span>

## <span data-ttu-id="1ef8a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ef8a-132">RELATED LINKS</span></span>
