---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334809"
---
# <span data-ttu-id="1fca7-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="1fca7-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="1fca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fca7-102">SYNOPSIS</span></span>
<span data-ttu-id="1fca7-103">서버에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="1fca7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1fca7-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fca7-105">설명</span><span class="sxs-lookup"><span data-stu-id="1fca7-105">DESCRIPTION</span></span>
<span data-ttu-id="1fca7-106">이 Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet은 Azure SQL 서버에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="1fca7-107">이 cmdlet을 사용하려면 ResourceGroupName 및 ServerName 매개 변수를 지정하여 이 cmdlet이 설정을 제거하는 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="1fca7-108">예제</span><span class="sxs-lookup"><span data-stu-id="1fca7-108">EXAMPLES</span></span>

### <span data-ttu-id="1fca7-109">예제 1: 데이터베이스에 대한 고급 위협 방지 설정 제거</span><span class="sxs-lookup"><span data-stu-id="1fca7-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="1fca7-110">이 명령은 Server01이라는 서버에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="1fca7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fca7-111">PARAMETERS</span></span>

### <span data-ttu-id="1fca7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fca7-112">-DefaultProfile</span></span>
<span data-ttu-id="1fca7-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1fca7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fca7-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fca7-114">-PassThru</span></span>
<span data-ttu-id="1fca7-115">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1fca7-116">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fca7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fca7-117">-ResourceGroupName</span></span>
<span data-ttu-id="1fca7-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="1fca7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fca7-119">-ServerName</span></span>
<span data-ttu-id="1fca7-120">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fca7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fca7-121">-Confirm</span></span>
<span data-ttu-id="1fca7-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fca7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fca7-123">-WhatIf</span></span>
<span data-ttu-id="1fca7-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1fca7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fca7-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fca7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fca7-126">CommonParameters</span></span>
<span data-ttu-id="1fca7-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1fca7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fca7-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1fca7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fca7-129">입력</span><span class="sxs-lookup"><span data-stu-id="1fca7-129">INPUTS</span></span>

### <span data-ttu-id="1fca7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1fca7-130">System.String</span></span>

## <span data-ttu-id="1fca7-131">출력</span><span class="sxs-lookup"><span data-stu-id="1fca7-131">OUTPUTS</span></span>

### <span data-ttu-id="1fca7-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="1fca7-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="1fca7-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1fca7-133">NOTES</span></span>

## <span data-ttu-id="1fca7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fca7-134">RELATED LINKS</span></span>

[<span data-ttu-id="1fca7-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="1fca7-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

