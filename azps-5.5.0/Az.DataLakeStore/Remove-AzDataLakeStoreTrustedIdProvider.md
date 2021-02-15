---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209789"
---
# <span data-ttu-id="2c677-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2c677-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="2c677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c677-102">SYNOPSIS</span></span>
<span data-ttu-id="2c677-103">지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2c677-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c677-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c677-105">설명</span><span class="sxs-lookup"><span data-stu-id="2c677-105">DESCRIPTION</span></span>
<span data-ttu-id="2c677-106">**Remove-AzDataLakeStoreTrustedIdProvider** cmdlet은 지정된 Data Lake Store에서 지정된 신뢰할 수 있는 ID 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2c677-107">예제</span><span class="sxs-lookup"><span data-stu-id="2c677-107">EXAMPLES</span></span>

### <span data-ttu-id="2c677-108">예제 1: 신뢰할 수 있는 ID 공급자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="2c677-109">"ContosoADL" 계정에서 공급자 "MyProvider"를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="2c677-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c677-110">PARAMETERS</span></span>

### <span data-ttu-id="2c677-111">-Account</span><span class="sxs-lookup"><span data-stu-id="2c677-111">-Account</span></span>
<span data-ttu-id="2c677-112">신뢰할 수 있는 ID 공급자를 제거할 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="2c677-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="2c677-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c677-113">-DefaultProfile</span></span>
<span data-ttu-id="2c677-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2c677-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c677-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2c677-115">-Name</span></span>
<span data-ttu-id="2c677-116">신뢰할 수 있는 ID 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="2c677-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c677-117">-PassThru</span></span>
<span data-ttu-id="2c677-118">삭제 작업의 결과를 나타내는 부울 응답이 반환되었음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c677-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c677-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c677-120">신뢰할 수 있는 ID 공급자를 제거할 계정이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c677-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c677-121">-Confirm</span></span>
<span data-ttu-id="2c677-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c677-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c677-123">-WhatIf</span></span>
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

### <span data-ttu-id="2c677-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c677-124">CommonParameters</span></span>
<span data-ttu-id="2c677-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c677-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c677-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2c677-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c677-127">입력</span><span class="sxs-lookup"><span data-stu-id="2c677-127">INPUTS</span></span>

### <span data-ttu-id="2c677-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2c677-128">System.String</span></span>

### <span data-ttu-id="2c677-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2c677-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c677-130">출력</span><span class="sxs-lookup"><span data-stu-id="2c677-130">OUTPUTS</span></span>

### <span data-ttu-id="2c677-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c677-131">System.Boolean</span></span>

## <span data-ttu-id="2c677-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c677-132">NOTES</span></span>

## <span data-ttu-id="2c677-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c677-133">RELATED LINKS</span></span>
