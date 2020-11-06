---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527627"
---
# <span data-ttu-id="aca77-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="aca77-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="aca77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca77-102">SYNOPSIS</span></span>
<span data-ttu-id="aca77-103">Azure Data Lake Analytics 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aca77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aca77-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aca77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aca77-105">DESCRIPTION</span></span>
<span data-ttu-id="aca77-106">Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="aca77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aca77-107">EXAMPLES</span></span>

### <span data-ttu-id="aca77-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="aca77-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="aca77-109">이 명령은 지정 된 Data Lake Analytics 카탈로그 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="aca77-110">변수</span><span class="sxs-lookup"><span data-stu-id="aca77-110">PARAMETERS</span></span>

### <span data-ttu-id="aca77-111">-계정</span><span class="sxs-lookup"><span data-stu-id="aca77-111">-Account</span></span>
<span data-ttu-id="aca77-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="aca77-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aca77-113">-DatabaseName</span></span>
<span data-ttu-id="aca77-114">자격 증명을 보유 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="aca77-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aca77-115">-Force</span></span>
<span data-ttu-id="aca77-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca77-117">-이름</span><span class="sxs-lookup"><span data-stu-id="aca77-117">-Name</span></span>
<span data-ttu-id="aca77-118">자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="aca77-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aca77-119">-PassThru</span></span>
<span data-ttu-id="aca77-120">이 cmdlet이 작업이 완료 될 때까지 대기 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="aca77-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aca77-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aca77-123">-암호</span><span class="sxs-lookup"><span data-stu-id="aca77-123">-Password</span></span>
<span data-ttu-id="aca77-124">자격 증명의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-124">The password for the credential.</span></span>
<span data-ttu-id="aca77-125">이는 호출자가 계정 소유자가 아닌 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-125">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aca77-126">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="aca77-126">-Recurse</span></span>
<span data-ttu-id="aca77-127">이 삭제 작업을 수행 하 고이 자격 증명에 종속 된 모든 리소스를 삭제 및 제거 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="aca77-128">-확인</span><span class="sxs-lookup"><span data-stu-id="aca77-128">-Confirm</span></span>
<span data-ttu-id="aca77-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca77-130">-WhatIf</span></span>
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

### <span data-ttu-id="aca77-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca77-131">-DefaultProfile</span></span>
<span data-ttu-id="aca77-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aca77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca77-133">CommonParameters</span></span>
<span data-ttu-id="aca77-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca77-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca77-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca77-136">입력</span><span class="sxs-lookup"><span data-stu-id="aca77-136">INPUTS</span></span>

## <span data-ttu-id="aca77-137">출력</span><span class="sxs-lookup"><span data-stu-id="aca77-137">OUTPUTS</span></span>

### <span data-ttu-id="aca77-138">부울</span><span class="sxs-lookup"><span data-stu-id="aca77-138">bool</span></span>
<span data-ttu-id="aca77-139">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aca77-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="aca77-140">상속자</span><span class="sxs-lookup"><span data-stu-id="aca77-140">NOTES</span></span>

## <span data-ttu-id="aca77-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aca77-141">RELATED LINKS</span></span>

