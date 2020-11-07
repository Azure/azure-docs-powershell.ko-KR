---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 79e5823c797c878643ea6ad2870873da363d0312
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696904"
---
# <span data-ttu-id="f4ea6-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="f4ea6-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="f4ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ea6-103">Azure Data Lake Analytics 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="f4ea6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4ea6-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ea6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f4ea6-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ea6-106">Remove-AzDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="f4ea6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f4ea6-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ea6-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="f4ea6-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="f4ea6-109">이 명령은 지정 된 Data Lake Analytics 카탈로그 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="f4ea6-110">변수</span><span class="sxs-lookup"><span data-stu-id="f4ea6-110">PARAMETERS</span></span>

### <span data-ttu-id="f4ea6-111">-계정</span><span class="sxs-lookup"><span data-stu-id="f4ea6-111">-Account</span></span>
<span data-ttu-id="f4ea6-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f4ea6-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4ea6-113">-DatabaseName</span></span>
<span data-ttu-id="f4ea6-114">자격 증명을 보유 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="f4ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="f4ea6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f4ea6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4ea6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f4ea6-117">-Force</span></span>
<span data-ttu-id="f4ea6-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4ea6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f4ea6-119">-Name</span></span>
<span data-ttu-id="f4ea6-120">자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="f4ea6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4ea6-121">-PassThru</span></span>
<span data-ttu-id="f4ea6-122">이 cmdlet이 작업이 완료 될 때까지 대기 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="f4ea6-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f4ea6-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4ea6-125">-암호</span><span class="sxs-lookup"><span data-stu-id="f4ea6-125">-Password</span></span>
<span data-ttu-id="f4ea6-126">자격 증명의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-126">The password for the credential.</span></span>
<span data-ttu-id="f4ea6-127">이는 호출자가 계정 소유자가 아닌 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="f4ea6-128">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="f4ea6-128">-Recurse</span></span>
<span data-ttu-id="f4ea6-129">이 삭제 작업을 수행 하 고이 자격 증명에 종속 된 모든 리소스를 삭제 및 제거 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="f4ea6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="f4ea6-130">-Confirm</span></span>
<span data-ttu-id="f4ea6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ea6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ea6-132">-WhatIf</span></span>
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

### <span data-ttu-id="f4ea6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ea6-133">CommonParameters</span></span>
<span data-ttu-id="f4ea6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ea6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ea6-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ea6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ea6-136">입력</span><span class="sxs-lookup"><span data-stu-id="f4ea6-136">INPUTS</span></span>

### <span data-ttu-id="f4ea6-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f4ea6-137">System.String</span></span>

### <span data-ttu-id="f4ea6-138">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="f4ea6-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="f4ea6-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4ea6-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4ea6-140">출력</span><span class="sxs-lookup"><span data-stu-id="f4ea6-140">OUTPUTS</span></span>

### <span data-ttu-id="f4ea6-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f4ea6-141">System.Boolean</span></span>

## <span data-ttu-id="f4ea6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f4ea6-142">NOTES</span></span>

## <span data-ttu-id="f4ea6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4ea6-143">RELATED LINKS</span></span>
