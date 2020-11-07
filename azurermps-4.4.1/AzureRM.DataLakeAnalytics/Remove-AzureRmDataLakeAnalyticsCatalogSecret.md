---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703773"
---
# <span data-ttu-id="e2315-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e2315-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="e2315-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2315-102">SYNOPSIS</span></span>
<span data-ttu-id="e2315-103">Data Lake Analytics 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2315-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2315-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2315-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2315-105">DESCRIPTION</span></span>
<span data-ttu-id="e2315-106">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet은 Azure Data Lake Analytics 카탈로그 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="e2315-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e2315-107">EXAMPLES</span></span>

### <span data-ttu-id="e2315-108">예제 1: 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="e2315-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="e2315-109">이 명령은 지정 된 Data Lake Analytics 카탈로그 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="e2315-110">변수</span><span class="sxs-lookup"><span data-stu-id="e2315-110">PARAMETERS</span></span>

### <span data-ttu-id="e2315-111">-계정</span><span class="sxs-lookup"><span data-stu-id="e2315-111">-Account</span></span>
<span data-ttu-id="e2315-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e2315-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2315-113">-DatabaseName</span></span>
<span data-ttu-id="e2315-114">비밀을 저장 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="e2315-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e2315-115">-Force</span></span>
<span data-ttu-id="e2315-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2315-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e2315-117">-Name</span></span>
<span data-ttu-id="e2315-118">비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-118">Specifies the name of the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2315-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2315-119">-PassThru</span></span>
<span data-ttu-id="e2315-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2315-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2315-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e2315-122">-Confirm</span></span>
<span data-ttu-id="e2315-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2315-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2315-124">-WhatIf</span></span>
<span data-ttu-id="e2315-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2315-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2315-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2315-127">-DefaultProfile</span></span>
<span data-ttu-id="e2315-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2315-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2315-129">CommonParameters</span></span>
<span data-ttu-id="e2315-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2315-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2315-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2315-132">입력</span><span class="sxs-lookup"><span data-stu-id="e2315-132">INPUTS</span></span>

## <span data-ttu-id="e2315-133">출력</span><span class="sxs-lookup"><span data-stu-id="e2315-133">OUTPUTS</span></span>

### <span data-ttu-id="e2315-134">부울</span><span class="sxs-lookup"><span data-stu-id="e2315-134">bool</span></span>
<span data-ttu-id="e2315-135">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2315-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="e2315-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e2315-136">NOTES</span></span>

## <span data-ttu-id="e2315-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2315-137">RELATED LINKS</span></span>

[<span data-ttu-id="e2315-138">새로운 AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e2315-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="e2315-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e2315-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


