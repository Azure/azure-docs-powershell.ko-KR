---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194809"
---
# <span data-ttu-id="3e505-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="3e505-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="3e505-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e505-102">SYNOPSIS</span></span>
<span data-ttu-id="3e505-103">Azure Data Lake Analytics 자격 증명을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="3e505-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e505-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e505-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e505-105">DESCRIPTION</span></span>
<span data-ttu-id="3e505-106">이 Remove-AzDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그 자격 증명을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="3e505-107">예제</span><span class="sxs-lookup"><span data-stu-id="3e505-107">EXAMPLES</span></span>

### <span data-ttu-id="3e505-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="3e505-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="3e505-109">이 명령은 지정된 Data Lake Analytics 카탈로그 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="3e505-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e505-110">PARAMETERS</span></span>

### <span data-ttu-id="3e505-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3e505-111">-Account</span></span>
<span data-ttu-id="3e505-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3e505-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e505-113">-DatabaseName</span></span>
<span data-ttu-id="3e505-114">자격 증명을 보유하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="3e505-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e505-115">-DefaultProfile</span></span>
<span data-ttu-id="3e505-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3e505-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e505-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3e505-117">-Force</span></span>
<span data-ttu-id="3e505-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e505-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3e505-119">-Name</span></span>
<span data-ttu-id="3e505-120">자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="3e505-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e505-121">-PassThru</span></span>
<span data-ttu-id="3e505-122">이 cmdlet이 작업이 완료될 때까지 기다리지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="3e505-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e505-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e505-125">-Password</span><span class="sxs-lookup"><span data-stu-id="3e505-125">-Password</span></span>
<span data-ttu-id="3e505-126">자격 증명에 대한 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-126">The password for the credential.</span></span>
<span data-ttu-id="3e505-127">호출자 계정 소유자가 아닌 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="3e505-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="3e505-128">-Recurse</span></span>
<span data-ttu-id="3e505-129">이 삭제 작업이 진행되고 이 자격 증명에 종속된 모든 리소스도 삭제하고 삭제해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="3e505-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e505-130">-Confirm</span></span>
<span data-ttu-id="3e505-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e505-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e505-132">-WhatIf</span></span>
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

### <span data-ttu-id="3e505-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e505-133">CommonParameters</span></span>
<span data-ttu-id="3e505-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e505-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e505-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3e505-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e505-136">입력</span><span class="sxs-lookup"><span data-stu-id="3e505-136">INPUTS</span></span>

### <span data-ttu-id="3e505-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3e505-137">System.String</span></span>

### <span data-ttu-id="3e505-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="3e505-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="3e505-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e505-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e505-140">출력</span><span class="sxs-lookup"><span data-stu-id="3e505-140">OUTPUTS</span></span>

### <span data-ttu-id="3e505-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e505-141">System.Boolean</span></span>

## <span data-ttu-id="3e505-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e505-142">NOTES</span></span>

## <span data-ttu-id="3e505-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e505-143">RELATED LINKS</span></span>
