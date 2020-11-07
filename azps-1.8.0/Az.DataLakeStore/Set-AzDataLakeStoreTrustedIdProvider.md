---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: cf35c2817e32045e3e0a9e236f1c92f7f273407c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868485"
---
# <span data-ttu-id="f1a1c-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f1a1c-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f1a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a1c-103">지정 된 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="f1a1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1a1c-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1a1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f1a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a1c-106">**AzDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="f1a1c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f1a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="f1a1c-108">예제 1: 신뢰할 수 있는 Id 공급자 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="f1a1c-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="f1a1c-109">이는 "ContosoADL" 계정에서 "MyProvider" 방화벽 규칙에 대 한 공급자 endpoing을 "" "로 업데이트 합니다. https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150</span><span class="sxs-lookup"><span data-stu-id="f1a1c-109">This updates the provider endpoing for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="f1a1c-110">변수</span><span class="sxs-lookup"><span data-stu-id="f1a1c-110">PARAMETERS</span></span>

### <span data-ttu-id="f1a1c-111">-계정</span><span class="sxs-lookup"><span data-stu-id="f1a1c-111">-Account</span></span>
<span data-ttu-id="f1a1c-112">신뢰할 수 있는 id 공급자를 추가 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="f1a1c-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="f1a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="f1a1c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f1a1c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1a1c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f1a1c-115">-Name</span></span>
<span data-ttu-id="f1a1c-116">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="f1a1c-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1a1c-117">-ProviderEndpoint</span></span>
<span data-ttu-id="f1a1c-118">유효한 신뢰할 수 있는 공급자 끝점 형식: https://sts.windows.net/\<provider id\></span><span class="sxs-lookup"><span data-stu-id="f1a1c-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="f1a1c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a1c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1a1c-120">신뢰할 수 있는 id 공급자를 업데이트할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="f1a1c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f1a1c-121">-Confirm</span></span>
<span data-ttu-id="f1a1c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a1c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a1c-123">-WhatIf</span></span>
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

### <span data-ttu-id="f1a1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a1c-124">CommonParameters</span></span>
<span data-ttu-id="f1a1c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a1c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a1c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a1c-127">입력</span><span class="sxs-lookup"><span data-stu-id="f1a1c-127">INPUTS</span></span>

### <span data-ttu-id="f1a1c-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1a1c-128">System.String</span></span>

## <span data-ttu-id="f1a1c-129">출력</span><span class="sxs-lookup"><span data-stu-id="f1a1c-129">OUTPUTS</span></span>

### <span data-ttu-id="f1a1c-130">DataLakeStore. DataLakeStoreTrustedIdProvider/.</span><span class="sxs-lookup"><span data-stu-id="f1a1c-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f1a1c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f1a1c-131">NOTES</span></span>

## <span data-ttu-id="f1a1c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1a1c-132">RELATED LINKS</span></span>
