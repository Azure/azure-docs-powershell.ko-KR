---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 3e16db29f6560778dff5c86ac222d06fd41a5807
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043843"
---
# <span data-ttu-id="cf621-101">Remove-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="cf621-101">Remove-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="cf621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf621-102">SYNOPSIS</span></span>
<span data-ttu-id="cf621-103">지정한 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cf621-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf621-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf621-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cf621-105">DESCRIPTION</span></span>
<span data-ttu-id="cf621-106">**AzDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-106">The **Remove-AzDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cf621-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cf621-107">EXAMPLES</span></span>

### <span data-ttu-id="cf621-108">예제 1: 신뢰할 수 있는 id 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="cf621-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="cf621-109">"ContosoADL" 계정에서 "MyProvider" 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="cf621-110">변수</span><span class="sxs-lookup"><span data-stu-id="cf621-110">PARAMETERS</span></span>

### <span data-ttu-id="cf621-111">-계정</span><span class="sxs-lookup"><span data-stu-id="cf621-111">-Account</span></span>
<span data-ttu-id="cf621-112">신뢰할 수 있는 id 공급자를 제거 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="cf621-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="cf621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf621-113">-DefaultProfile</span></span>
<span data-ttu-id="cf621-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cf621-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf621-115">-이름</span><span class="sxs-lookup"><span data-stu-id="cf621-115">-Name</span></span>
<span data-ttu-id="cf621-116">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-116">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="cf621-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf621-117">-PassThru</span></span>
<span data-ttu-id="cf621-118">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="cf621-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf621-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf621-120">신뢰할 수 있는 id 공급자를 제거할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="cf621-121">-확인</span><span class="sxs-lookup"><span data-stu-id="cf621-121">-Confirm</span></span>
<span data-ttu-id="cf621-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf621-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf621-123">-WhatIf</span></span>
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

### <span data-ttu-id="cf621-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf621-124">CommonParameters</span></span>
<span data-ttu-id="cf621-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf621-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf621-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf621-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf621-127">입력</span><span class="sxs-lookup"><span data-stu-id="cf621-127">INPUTS</span></span>

### <span data-ttu-id="cf621-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf621-128">System.String</span></span>

### <span data-ttu-id="cf621-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cf621-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cf621-130">출력</span><span class="sxs-lookup"><span data-stu-id="cf621-130">OUTPUTS</span></span>

### <span data-ttu-id="cf621-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cf621-131">System.Boolean</span></span>

## <span data-ttu-id="cf621-132">상속자</span><span class="sxs-lookup"><span data-stu-id="cf621-132">NOTES</span></span>

## <span data-ttu-id="cf621-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf621-133">RELATED LINKS</span></span>
