---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 2ee08eaf9dae9a6d2001608d8ef247c7e116c98e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528985"
---
# <span data-ttu-id="ffb98-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="ffb98-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="ffb98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb98-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb98-103">Data Lake Analytics 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffb98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffb98-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffb98-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb98-106">**AzureRmDataLakeAnalyticsCatalogSecret** Cmdlet은 Azure Data Lake Analytics 카탈로그 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="ffb98-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ffb98-107">EXAMPLES</span></span>

### <span data-ttu-id="ffb98-108">예제 1: 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="ffb98-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="ffb98-109">이 명령은 지정 된 Data Lake Analytics 카탈로그 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="ffb98-110">변수</span><span class="sxs-lookup"><span data-stu-id="ffb98-110">PARAMETERS</span></span>

### <span data-ttu-id="ffb98-111">-계정</span><span class="sxs-lookup"><span data-stu-id="ffb98-111">-Account</span></span>
<span data-ttu-id="ffb98-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ffb98-113">-DatabaseName</span></span>
<span data-ttu-id="ffb98-114">비밀을 저장 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-114">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb98-115">-DefaultProfile</span></span>
<span data-ttu-id="ffb98-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ffb98-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ffb98-117">-Force</span></span>
<span data-ttu-id="ffb98-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ffb98-119">-Name</span></span>
<span data-ttu-id="ffb98-120">비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-120">Specifies the name of the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffb98-121">-PassThru</span></span>
<span data-ttu-id="ffb98-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ffb98-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ffb98-124">-Confirm</span></span>
<span data-ttu-id="ffb98-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb98-126">-WhatIf</span></span>
<span data-ttu-id="ffb98-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb98-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffb98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb98-129">CommonParameters</span></span>
<span data-ttu-id="ffb98-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb98-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffb98-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb98-132">입력</span><span class="sxs-lookup"><span data-stu-id="ffb98-132">INPUTS</span></span>

### <span data-ttu-id="ffb98-133">않아야</span><span class="sxs-lookup"><span data-stu-id="ffb98-133">None</span></span>
<span data-ttu-id="ffb98-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ffb98-135">출력</span><span class="sxs-lookup"><span data-stu-id="ffb98-135">OUTPUTS</span></span>

### <span data-ttu-id="ffb98-136">부울</span><span class="sxs-lookup"><span data-stu-id="ffb98-136">bool</span></span>
<span data-ttu-id="ffb98-137">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffb98-137">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="ffb98-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ffb98-138">NOTES</span></span>

## <span data-ttu-id="ffb98-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffb98-139">RELATED LINKS</span></span>

[<span data-ttu-id="ffb98-140">새로운 AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="ffb98-140">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="ffb98-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="ffb98-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


