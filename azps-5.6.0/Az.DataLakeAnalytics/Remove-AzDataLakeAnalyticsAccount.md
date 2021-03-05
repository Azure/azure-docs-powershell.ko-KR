---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 29846c8bb5650a667bf565fec273cbf24c8cd394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004256"
---
# <span data-ttu-id="9ac30-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9ac30-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="9ac30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac30-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac30-103">Data Lake Analytics 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9ac30-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ac30-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ac30-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ac30-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac30-106">**Remove-AzDataLakeAnalyticsAccount** cmdlet은 Azure Data Lake Analytics 계정을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9ac30-107">예제</span><span class="sxs-lookup"><span data-stu-id="9ac30-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac30-108">예제 1: 계정 제거</span><span class="sxs-lookup"><span data-stu-id="9ac30-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="9ac30-109">이 명령은 지정된 Data Lake Analytics 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="9ac30-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9ac30-110">PARAMETERS</span></span>

### <span data-ttu-id="9ac30-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac30-111">-DefaultProfile</span></span>
<span data-ttu-id="9ac30-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ac30-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ac30-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9ac30-113">-Force</span></span>
<span data-ttu-id="9ac30-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ac30-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9ac30-115">-Name</span></span>
<span data-ttu-id="9ac30-116">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9ac30-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ac30-117">-PassThru</span></span>
<span data-ttu-id="9ac30-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ac30-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ac30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac30-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ac30-121">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="9ac30-122">-확인</span><span class="sxs-lookup"><span data-stu-id="9ac30-122">-Confirm</span></span>
<span data-ttu-id="9ac30-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ac30-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ac30-124">-WhatIf</span></span>
<span data-ttu-id="9ac30-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ac30-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ac30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac30-127">CommonParameters</span></span>
<span data-ttu-id="9ac30-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac30-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ac30-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac30-130">입력</span><span class="sxs-lookup"><span data-stu-id="9ac30-130">INPUTS</span></span>

### <span data-ttu-id="9ac30-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9ac30-131">System.String</span></span>

## <span data-ttu-id="9ac30-132">출력</span><span class="sxs-lookup"><span data-stu-id="9ac30-132">OUTPUTS</span></span>

### <span data-ttu-id="9ac30-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ac30-133">System.Boolean</span></span>

## <span data-ttu-id="9ac30-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ac30-134">NOTES</span></span>

## <span data-ttu-id="9ac30-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ac30-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ac30-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9ac30-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9ac30-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9ac30-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9ac30-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9ac30-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9ac30-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9ac30-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


