---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339609"
---
# <span data-ttu-id="0bd00-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0bd00-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0bd00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd00-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd00-103">Data Lake Analytics 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="0bd00-104">구문</span><span class="sxs-lookup"><span data-stu-id="0bd00-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd00-105">설명</span><span class="sxs-lookup"><span data-stu-id="0bd00-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd00-106">**Remove-AzDataLakeAnalyticsAccount** cmdlet은 Azure Data Lake Analytics 계정을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0bd00-107">예제</span><span class="sxs-lookup"><span data-stu-id="0bd00-107">EXAMPLES</span></span>

### <span data-ttu-id="0bd00-108">예제 1: 계정 제거</span><span class="sxs-lookup"><span data-stu-id="0bd00-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0bd00-109">이 명령은 지정된 Data Lake Analytics 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="0bd00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bd00-110">PARAMETERS</span></span>

### <span data-ttu-id="0bd00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd00-111">-DefaultProfile</span></span>
<span data-ttu-id="0bd00-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0bd00-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bd00-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0bd00-113">-Force</span></span>
<span data-ttu-id="0bd00-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bd00-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0bd00-115">-Name</span></span>
<span data-ttu-id="0bd00-116">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd00-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bd00-117">-PassThru</span></span>
<span data-ttu-id="0bd00-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0bd00-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bd00-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd00-120">-ResourceGroupName</span></span>
<span data-ttu-id="0bd00-121">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0bd00-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bd00-122">-Confirm</span></span>
<span data-ttu-id="0bd00-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bd00-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bd00-124">-WhatIf</span></span>
<span data-ttu-id="0bd00-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0bd00-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bd00-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bd00-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd00-127">CommonParameters</span></span>
<span data-ttu-id="0bd00-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0bd00-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd00-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0bd00-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd00-130">입력</span><span class="sxs-lookup"><span data-stu-id="0bd00-130">INPUTS</span></span>

### <span data-ttu-id="0bd00-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0bd00-131">System.String</span></span>

## <span data-ttu-id="0bd00-132">출력</span><span class="sxs-lookup"><span data-stu-id="0bd00-132">OUTPUTS</span></span>

### <span data-ttu-id="0bd00-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0bd00-133">System.Boolean</span></span>

## <span data-ttu-id="0bd00-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0bd00-134">NOTES</span></span>

## <span data-ttu-id="0bd00-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bd00-135">RELATED LINKS</span></span>

[<span data-ttu-id="0bd00-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0bd00-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0bd00-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0bd00-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0bd00-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0bd00-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0bd00-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0bd00-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


