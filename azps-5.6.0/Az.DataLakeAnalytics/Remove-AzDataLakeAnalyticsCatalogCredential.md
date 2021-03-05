---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: f14448e7b7606f37f5ffdee8c944d48a557c1f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998382"
---
# <span data-ttu-id="3d95d-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="3d95d-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="3d95d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d95d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d95d-103">Azure Data Lake Analytics 자격 증명을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="3d95d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d95d-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d95d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d95d-105">DESCRIPTION</span></span>
<span data-ttu-id="3d95d-106">Remove-AzDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그 자격 증명을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="3d95d-107">예제</span><span class="sxs-lookup"><span data-stu-id="3d95d-107">EXAMPLES</span></span>

### <span data-ttu-id="3d95d-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="3d95d-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="3d95d-109">이 명령은 지정된 Data Lake Analytics 카탈로그 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="3d95d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d95d-110">PARAMETERS</span></span>

### <span data-ttu-id="3d95d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3d95d-111">-Account</span></span>
<span data-ttu-id="3d95d-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3d95d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d95d-113">-DatabaseName</span></span>
<span data-ttu-id="3d95d-114">자격 증명을 보유하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="3d95d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d95d-115">-DefaultProfile</span></span>
<span data-ttu-id="3d95d-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d95d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d95d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3d95d-117">-Force</span></span>
<span data-ttu-id="3d95d-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d95d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3d95d-119">-Name</span></span>
<span data-ttu-id="3d95d-120">자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="3d95d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d95d-121">-PassThru</span></span>
<span data-ttu-id="3d95d-122">이 cmdlet이 작업이 완료될 때까지 기다릴 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="3d95d-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3d95d-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3d95d-125">-Password</span><span class="sxs-lookup"><span data-stu-id="3d95d-125">-Password</span></span>
<span data-ttu-id="3d95d-126">자격 증명에 대한 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-126">The password for the credential.</span></span>
<span data-ttu-id="3d95d-127">이는 호출자가 계정의 소유자가 아닌 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="3d95d-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="3d95d-128">-Recurse</span></span>
<span data-ttu-id="3d95d-129">이 삭제 작업은 이 자격 증명에 종속된 모든 리소스를 삭제하고 삭제해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="3d95d-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3d95d-130">-Confirm</span></span>
<span data-ttu-id="3d95d-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d95d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d95d-132">-WhatIf</span></span>
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

### <span data-ttu-id="3d95d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d95d-133">CommonParameters</span></span>
<span data-ttu-id="3d95d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d95d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d95d-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3d95d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d95d-136">입력</span><span class="sxs-lookup"><span data-stu-id="3d95d-136">INPUTS</span></span>

### <span data-ttu-id="3d95d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3d95d-137">System.String</span></span>

### <span data-ttu-id="3d95d-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="3d95d-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="3d95d-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d95d-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d95d-140">출력</span><span class="sxs-lookup"><span data-stu-id="3d95d-140">OUTPUTS</span></span>

### <span data-ttu-id="3d95d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d95d-141">System.Boolean</span></span>

## <span data-ttu-id="3d95d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d95d-142">NOTES</span></span>

## <span data-ttu-id="3d95d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d95d-143">RELATED LINKS</span></span>
