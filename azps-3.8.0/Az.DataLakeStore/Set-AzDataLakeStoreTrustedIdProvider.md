---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045023"
---
# <span data-ttu-id="07ea3-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="07ea3-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="07ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="07ea3-103">지정 된 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ea3-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="07ea3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07ea3-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07ea3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="07ea3-106">**AzDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ea3-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="07ea3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="07ea3-108">예제 1: 신뢰할 수 있는 Id 공급자 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="07ea3-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="07ea3-109">이렇게 하면 "ContosoADL" 계정의 방화벽 규칙 "MyProvider"에 대 한 공급자 끝점이 "" "로 업데이트 됩니다. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="07ea3-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="07ea3-110">변수</span><span class="sxs-lookup"><span data-stu-id="07ea3-110">PARAMETERS</span></span>

### <span data-ttu-id="07ea3-111">-계정</span><span class="sxs-lookup"><span data-stu-id="07ea3-111">-Account</span></span>
<span data-ttu-id="07ea3-112">신뢰할 수 있는 id 공급자를 추가 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="07ea3-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="07ea3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ea3-113">-DefaultProfile</span></span>
<span data-ttu-id="07ea3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="07ea3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07ea3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="07ea3-115">-Name</span></span>
<span data-ttu-id="07ea3-116">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07ea3-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="07ea3-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="07ea3-117">-ProviderEndpoint</span></span>
<span data-ttu-id="07ea3-118">유효한 신뢰할 수 있는 공급자 끝점 형식: https://sts.windows.net/\<provider id\></span><span class="sxs-lookup"><span data-stu-id="07ea3-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="07ea3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ea3-119">-ResourceGroupName</span></span>
<span data-ttu-id="07ea3-120">신뢰할 수 있는 id 공급자를 업데이트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ea3-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="07ea3-121">-확인</span><span class="sxs-lookup"><span data-stu-id="07ea3-121">-Confirm</span></span>
<span data-ttu-id="07ea3-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ea3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ea3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ea3-123">-WhatIf</span></span>
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

### <span data-ttu-id="07ea3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ea3-124">CommonParameters</span></span>
<span data-ttu-id="07ea3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07ea3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ea3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ea3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ea3-127">입력</span><span class="sxs-lookup"><span data-stu-id="07ea3-127">INPUTS</span></span>

### <span data-ttu-id="07ea3-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07ea3-128">System.String</span></span>

## <span data-ttu-id="07ea3-129">출력</span><span class="sxs-lookup"><span data-stu-id="07ea3-129">OUTPUTS</span></span>

### <span data-ttu-id="07ea3-130">DataLakeStore. DataLakeStoreTrustedIdProvider/.</span><span class="sxs-lookup"><span data-stu-id="07ea3-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="07ea3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="07ea3-131">NOTES</span></span>

## <span data-ttu-id="07ea3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07ea3-132">RELATED LINKS</span></span>
