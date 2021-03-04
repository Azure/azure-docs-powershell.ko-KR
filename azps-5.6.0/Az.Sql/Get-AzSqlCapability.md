---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 7c45cb511fe1466aa2ac210ceeb2b609f6c0e97a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993267"
---
# <span data-ttu-id="b9bab-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b9bab-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="b9bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9bab-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bab-103">현재 SQL 데이터베이스 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="b9bab-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9bab-104">SYNTAX</span></span>

### <span data-ttu-id="b9bab-105">FilterResults(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9bab-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9bab-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="b9bab-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9bab-107">설명</span><span class="sxs-lookup"><span data-stu-id="b9bab-107">DESCRIPTION</span></span>
<span data-ttu-id="b9bab-108">**Get-AzSqlCapability** cmdlet은 지역에 대한 현재 SQL Azure SQL 데이터베이스 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="b9bab-109">*ServerVersionName,* *EditionName* 또는 *ServiceObjectiveName* 매개 변수를 지정하는 경우 이 cmdlet은 지정된 값과 해당 선행 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="b9bab-110">예제</span><span class="sxs-lookup"><span data-stu-id="b9bab-110">EXAMPLES</span></span>

### <span data-ttu-id="b9bab-111">예제 1: 지역에 대한 현재 구독에 대한 기능 얻기</span><span class="sxs-lookup"><span data-stu-id="b9bab-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="b9bab-112">이 명령은 미국 중부 지역에 대한 현재 SQL 데이터베이스 인스턴스에 대한 기능을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="b9bab-113">예제 2: 지역에 대한 현재 구독에 대한 기본 기능 사용</span><span class="sxs-lookup"><span data-stu-id="b9bab-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="b9bab-114">이 명령은 미국 중부 지역의 현재 SQL 데이터베이스에 대한 기본 기능을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="b9bab-115">예제 3: 서비스 목표에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="b9bab-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="b9bab-116">이 명령은 현재 구독에서 지정된 SQL 데이터베이스에 대한 기본 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="b9bab-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9bab-117">PARAMETERS</span></span>

### <span data-ttu-id="b9bab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bab-118">-DefaultProfile</span></span>
<span data-ttu-id="b9bab-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b9bab-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9bab-120">-Defaults</span><span class="sxs-lookup"><span data-stu-id="b9bab-120">-Defaults</span></span>
<span data-ttu-id="b9bab-121">이 cmdlet은 기본값만 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9bab-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="b9bab-122">-EditionName</span></span>
<span data-ttu-id="b9bab-123">이 cmdlet이 기능을 얻을 데이터베이스 버전의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9bab-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="b9bab-124">-LocationName</span></span>
<span data-ttu-id="b9bab-125">이 cmdlet에서 기능을 얻을 위치의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="b9bab-126">자세한 내용은 Azure http://azure.microsoft.com/en-us/regions/ Regions(를 http://azure.microsoft.com/en-us/regions/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9bab-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="b9bab-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="b9bab-127">-ServerVersionName</span></span>
<span data-ttu-id="b9bab-128">이 cmdlet에서 기능을 얻을 수 있는 서버 버전의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9bab-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b9bab-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="b9bab-130">이 cmdlet에서 기능을 제공하는 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9bab-131">-확인</span><span class="sxs-lookup"><span data-stu-id="b9bab-131">-Confirm</span></span>
<span data-ttu-id="b9bab-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9bab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9bab-133">-WhatIf</span></span>
<span data-ttu-id="b9bab-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9bab-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9bab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bab-136">CommonParameters</span></span>
<span data-ttu-id="b9bab-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9bab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bab-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9bab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bab-139">입력</span><span class="sxs-lookup"><span data-stu-id="b9bab-139">INPUTS</span></span>

### <span data-ttu-id="b9bab-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b9bab-140">System.String</span></span>

## <span data-ttu-id="b9bab-141">출력</span><span class="sxs-lookup"><span data-stu-id="b9bab-141">OUTPUTS</span></span>

### <span data-ttu-id="b9bab-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="b9bab-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="b9bab-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9bab-143">NOTES</span></span>

## <span data-ttu-id="b9bab-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9bab-144">RELATED LINKS</span></span>
