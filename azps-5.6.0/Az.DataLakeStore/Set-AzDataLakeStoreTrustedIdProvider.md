---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 7efe0e21b6b433160eab36856d3419dc918cbfc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995591"
---
# <span data-ttu-id="4d605-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4d605-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4d605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d605-102">SYNOPSIS</span></span>
<span data-ttu-id="4d605-103">지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="4d605-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d605-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d605-105">설명</span><span class="sxs-lookup"><span data-stu-id="4d605-105">DESCRIPTION</span></span>
<span data-ttu-id="4d605-106">**Set-AzDataLakeStoreTrustedIdProvider** cmdlet은 지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="4d605-107">예제</span><span class="sxs-lookup"><span data-stu-id="4d605-107">EXAMPLES</span></span>

### <span data-ttu-id="4d605-108">예제 1: 신뢰할 수 있는 ID 공급자 엔드포인트 업데이트</span><span class="sxs-lookup"><span data-stu-id="4d605-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="4d605-109">그러면 "ContosoADL"의 방화벽 규칙 "MyProvider"에 대한 공급자 엔드포인트가 ""로 https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="4d605-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d605-110">PARAMETERS</span></span>

### <span data-ttu-id="4d605-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4d605-111">-Account</span></span>
<span data-ttu-id="4d605-112">신뢰할 수 있는 ID 공급자를 추가하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="4d605-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="4d605-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d605-113">-DefaultProfile</span></span>
<span data-ttu-id="4d605-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4d605-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d605-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4d605-115">-Name</span></span>
<span data-ttu-id="4d605-116">신뢰할 수 있는 ID 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="4d605-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d605-117">-ProviderEndpoint</span></span>
<span data-ttu-id="4d605-118">형식의 유효한 신뢰할 수 있는 공급자 엔드포인트: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="4d605-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="4d605-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d605-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d605-120">신뢰할 수 있는 ID 공급자를 업데이트할 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="4d605-121">-확인</span><span class="sxs-lookup"><span data-stu-id="4d605-121">-Confirm</span></span>
<span data-ttu-id="4d605-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d605-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d605-123">-WhatIf</span></span>
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

### <span data-ttu-id="4d605-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d605-124">CommonParameters</span></span>
<span data-ttu-id="4d605-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d605-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d605-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4d605-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d605-127">입력</span><span class="sxs-lookup"><span data-stu-id="4d605-127">INPUTS</span></span>

### <span data-ttu-id="4d605-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4d605-128">System.String</span></span>

## <span data-ttu-id="4d605-129">출력</span><span class="sxs-lookup"><span data-stu-id="4d605-129">OUTPUTS</span></span>

### <span data-ttu-id="4d605-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="4d605-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="4d605-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d605-131">NOTES</span></span>

## <span data-ttu-id="4d605-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d605-132">RELATED LINKS</span></span>
