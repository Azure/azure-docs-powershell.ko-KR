---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: b6647ab3b729ab76d3cc02687bcd8dc342e788b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489196"
---
# <span data-ttu-id="d2485-101">Add-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d2485-101">Add-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d2485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2485-102">SYNOPSIS</span></span>
<span data-ttu-id="d2485-103">지정된 Data Lake Store 계정에 신뢰할 수 있는 ID 공급자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d2485-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2485-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2485-105">설명</span><span class="sxs-lookup"><span data-stu-id="d2485-105">DESCRIPTION</span></span>
<span data-ttu-id="d2485-106">**Add-AzDataLakeStoreTrustedIdProvider** cmdlet은 지정된 Data Lake Store 계정에 신뢰할 수 있는 ID 공급자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-106">The **Add-AzDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d2485-107">예제</span><span class="sxs-lookup"><span data-stu-id="d2485-107">EXAMPLES</span></span>

### <span data-ttu-id="d2485-108">예제 1: 신뢰할 수 있는 ID 공급자 추가</span><span class="sxs-lookup"><span data-stu-id="d2485-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="d2485-109">공급자 엔드포인트 ""를 통해 "ContosoADL"을 계정에 "MyProvider"를 https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="d2485-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2485-110">PARAMETERS</span></span>

### <span data-ttu-id="d2485-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d2485-111">-Account</span></span>
<span data-ttu-id="d2485-112">지정된 신뢰할 수 있는 ID 공급자를 추가할 Data Lake Store 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

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

### <span data-ttu-id="d2485-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2485-113">-DefaultProfile</span></span>
<span data-ttu-id="d2485-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d2485-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2485-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d2485-115">-Name</span></span>
<span data-ttu-id="d2485-116">추가할 신뢰할 수 있는 ID 공급자의 이름</span><span class="sxs-lookup"><span data-stu-id="d2485-116">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="d2485-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2485-117">-ProviderEndpoint</span></span>
<span data-ttu-id="d2485-118">유효한 신뢰할 수 있는 공급자 엔드포인트 형식: https://sts.windows.net/ \<provider identity\> "</span><span class="sxs-lookup"><span data-stu-id="d2485-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

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

### <span data-ttu-id="d2485-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2485-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2485-120">신뢰할 수 있는 ID 공급자를 추가할 계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-120">Name of resource group under which the account to add the trusted identity provider is.</span></span>

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

### <span data-ttu-id="d2485-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2485-121">-Confirm</span></span>
<span data-ttu-id="d2485-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2485-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2485-123">-WhatIf</span></span>
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

### <span data-ttu-id="d2485-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2485-124">CommonParameters</span></span>
<span data-ttu-id="d2485-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2485-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2485-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d2485-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2485-127">입력</span><span class="sxs-lookup"><span data-stu-id="d2485-127">INPUTS</span></span>

### <span data-ttu-id="d2485-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d2485-128">System.String</span></span>

## <span data-ttu-id="d2485-129">출력</span><span class="sxs-lookup"><span data-stu-id="d2485-129">OUTPUTS</span></span>

### <span data-ttu-id="d2485-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="d2485-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="d2485-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2485-131">NOTES</span></span>

## <span data-ttu-id="d2485-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2485-132">RELATED LINKS</span></span>
