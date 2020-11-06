---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 089dbc5e3ca1d6a4a2a6528cb0c4bc87cf9b3dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538192"
---
# <span data-ttu-id="86c48-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="86c48-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="86c48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c48-102">SYNOPSIS</span></span>
<span data-ttu-id="86c48-103">지정한 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86c48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86c48-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86c48-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86c48-105">DESCRIPTION</span></span>
<span data-ttu-id="86c48-106">**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="86c48-107">예제의</span><span class="sxs-lookup"><span data-stu-id="86c48-107">EXAMPLES</span></span>

### <span data-ttu-id="86c48-108">예제 1: 신뢰할 수 있는 id 공급자 제거</span><span class="sxs-lookup"><span data-stu-id="86c48-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="86c48-109">"ContosoADL" 계정에서 "MyProvider" 공급자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="86c48-110">변수</span><span class="sxs-lookup"><span data-stu-id="86c48-110">PARAMETERS</span></span>

### <span data-ttu-id="86c48-111">-계정</span><span class="sxs-lookup"><span data-stu-id="86c48-111">-Account</span></span>
<span data-ttu-id="86c48-112">신뢰할 수 있는 id 공급자를 제거 하는 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="86c48-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

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

### <span data-ttu-id="86c48-113">-이름</span><span class="sxs-lookup"><span data-stu-id="86c48-113">-Name</span></span>
<span data-ttu-id="86c48-114">신뢰할 수 있는 id 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-114">The name of the trusted identity provider.</span></span>

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

### <span data-ttu-id="86c48-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c48-115">-PassThru</span></span>
<span data-ttu-id="86c48-116">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="86c48-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c48-117">-ResourceGroupName</span></span>
<span data-ttu-id="86c48-118">신뢰할 수 있는 id 공급자를 제거할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-118">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

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

### <span data-ttu-id="86c48-119">-확인</span><span class="sxs-lookup"><span data-stu-id="86c48-119">-Confirm</span></span>
<span data-ttu-id="86c48-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c48-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c48-121">-WhatIf</span></span>
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

### <span data-ttu-id="86c48-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c48-122">-DefaultProfile</span></span>
<span data-ttu-id="86c48-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86c48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c48-124">CommonParameters</span></span>
<span data-ttu-id="86c48-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c48-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c48-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c48-127">입력</span><span class="sxs-lookup"><span data-stu-id="86c48-127">INPUTS</span></span>

## <span data-ttu-id="86c48-128">출력</span><span class="sxs-lookup"><span data-stu-id="86c48-128">OUTPUTS</span></span>

### <span data-ttu-id="86c48-129">부울</span><span class="sxs-lookup"><span data-stu-id="86c48-129">bool</span></span>
<span data-ttu-id="86c48-130">PassThru가 지정 된 경우 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c48-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="86c48-131">상속자</span><span class="sxs-lookup"><span data-stu-id="86c48-131">NOTES</span></span>

## <span data-ttu-id="86c48-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86c48-132">RELATED LINKS</span></span>

