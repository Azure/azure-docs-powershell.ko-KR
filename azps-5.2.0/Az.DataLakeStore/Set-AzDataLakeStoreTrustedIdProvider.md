---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BDEF8BAA-0C64-465D-9ED4-6FEFC1E850CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c4de7a926e4095ad8bb45a25647305617988330d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330321"
---
# <span data-ttu-id="196b9-101">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="196b9-101">Set-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="196b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="196b9-102">SYNOPSIS</span></span>
<span data-ttu-id="196b9-103">지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-103">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="196b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="196b9-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="196b9-105">설명</span><span class="sxs-lookup"><span data-stu-id="196b9-105">DESCRIPTION</span></span>
<span data-ttu-id="196b9-106">**Set-AzDataLakeStoreTrustedIdProvider** cmdlet은 지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-106">The **Set-AzDataLakeStoreTrustedIdProvider** cmdlet modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="196b9-107">예제</span><span class="sxs-lookup"><span data-stu-id="196b9-107">EXAMPLES</span></span>

### <span data-ttu-id="196b9-108">예제 1: 신뢰할 수 있는 ID 공급자 엔드포인트 업데이트</span><span class="sxs-lookup"><span data-stu-id="196b9-108">Example 1: Update a Trusted Identity Provider Endpoint</span></span>
```
PS C:\> Set-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="196b9-109">"ContosoADL" 계정의 방화벽 규칙 "MyProvider"에 대한 공급자 엔드포인트를 ""로 https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-109">This updates the provider endpoint for firewall rule "MyProvider" in account "ContosoADL" to "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="196b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="196b9-110">PARAMETERS</span></span>

### <span data-ttu-id="196b9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="196b9-111">-Account</span></span>
<span data-ttu-id="196b9-112">신뢰할 수 있는 ID 공급자를 추가할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="196b9-112">The Data Lake Store account to add the trusted identity provider to</span></span>

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

### <span data-ttu-id="196b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196b9-113">-DefaultProfile</span></span>
<span data-ttu-id="196b9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="196b9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="196b9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="196b9-115">-Name</span></span>
<span data-ttu-id="196b9-116">신뢰할 수 있는 ID 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="196b9-117">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="196b9-117">-ProviderEndpoint</span></span>
<span data-ttu-id="196b9-118">유효한 신뢰할 수 있는 공급자 엔드포인트 형식: https://sts.windows.net/\<provider identity\></span><span class="sxs-lookup"><span data-stu-id="196b9-118">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\></span></span>

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

### <span data-ttu-id="196b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="196b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="196b9-120">신뢰할 수 있는 ID 공급자를 업데이트할 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-120">Specifies the name of the resource group that contains the account to update the trusted identity provider for.</span></span>

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

### <span data-ttu-id="196b9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="196b9-121">-Confirm</span></span>
<span data-ttu-id="196b9-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196b9-123">-WhatIf</span></span>
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

### <span data-ttu-id="196b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196b9-124">CommonParameters</span></span>
<span data-ttu-id="196b9-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="196b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196b9-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="196b9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196b9-127">입력</span><span class="sxs-lookup"><span data-stu-id="196b9-127">INPUTS</span></span>

### <span data-ttu-id="196b9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="196b9-128">System.String</span></span>

## <span data-ttu-id="196b9-129">출력</span><span class="sxs-lookup"><span data-stu-id="196b9-129">OUTPUTS</span></span>

### <span data-ttu-id="196b9-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="196b9-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="196b9-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="196b9-131">NOTES</span></span>

## <span data-ttu-id="196b9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="196b9-132">RELATED LINKS</span></span>
