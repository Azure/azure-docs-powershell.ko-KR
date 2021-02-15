---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197772"
---
# <span data-ttu-id="61fec-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="61fec-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="61fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61fec-102">SYNOPSIS</span></span>
<span data-ttu-id="61fec-103">현재 SQL 데이터베이스 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="61fec-104">구문</span><span class="sxs-lookup"><span data-stu-id="61fec-104">SYNTAX</span></span>

### <span data-ttu-id="61fec-105">FilterResults(기본값)</span><span class="sxs-lookup"><span data-stu-id="61fec-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61fec-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="61fec-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61fec-107">설명</span><span class="sxs-lookup"><span data-stu-id="61fec-107">DESCRIPTION</span></span>
<span data-ttu-id="61fec-108">**Get-AzSqlCapability** cmdlet은 Azure SQL 데이터베이스 기능을 지역의 현재 구독에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="61fec-109">*ServerVersionName,* *EditionName* 또는 *ServiceObjectiveName* 매개 변수를 지정하는 경우 이 cmdlet은 지정된 값과 해당 선행 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="61fec-110">예제</span><span class="sxs-lookup"><span data-stu-id="61fec-110">EXAMPLES</span></span>

### <span data-ttu-id="61fec-111">예제 1: 지역에 대한 현재 구독에 대한 기능 얻기</span><span class="sxs-lookup"><span data-stu-id="61fec-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="61fec-112">이 명령은 미국 중부 지역의 현재 SQL 데이터베이스 인스턴스에 대한 기능을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="61fec-113">예제 2: 지역에 대한 현재 구독에 대한 기본 기능 얻기</span><span class="sxs-lookup"><span data-stu-id="61fec-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="61fec-114">이 명령은 미국 중부 지역의 현재 SQL 데이터베이스에 대한 기본 기능을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="61fec-115">예제 3: 서비스 목표에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="61fec-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="61fec-116">이 명령은 현재 구독에서 지정된 SQL 데이터베이스에 대한 기본 기능을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="61fec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61fec-117">PARAMETERS</span></span>

### <span data-ttu-id="61fec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fec-118">-DefaultProfile</span></span>
<span data-ttu-id="61fec-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="61fec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61fec-120">-Defaults</span><span class="sxs-lookup"><span data-stu-id="61fec-120">-Defaults</span></span>
<span data-ttu-id="61fec-121">이 cmdlet이 기본값만 얻게 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-121">Indicates that this cmdlet gets only defaults.</span></span>

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

### <span data-ttu-id="61fec-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="61fec-122">-EditionName</span></span>
<span data-ttu-id="61fec-123">이 cmdlet이 기능을 사용할 데이터베이스 버전 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="61fec-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="61fec-124">-LocationName</span></span>
<span data-ttu-id="61fec-125">이 cmdlet이 기능을 얻을 위치의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="61fec-126">자세한 내용은 Azure http://azure.microsoft.com/en-us/regions/ http://azure.microsoft.com/en-us/regions/) 지역(.</span><span class="sxs-lookup"><span data-stu-id="61fec-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="61fec-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="61fec-127">-ServerVersionName</span></span>
<span data-ttu-id="61fec-128">이 cmdlet이 기능을 사용할 서버 버전의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="61fec-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="61fec-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="61fec-130">이 cmdlet이 기능을 얻을 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="61fec-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61fec-131">-Confirm</span></span>
<span data-ttu-id="61fec-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61fec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61fec-133">-WhatIf</span></span>
<span data-ttu-id="61fec-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="61fec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61fec-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61fec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fec-136">CommonParameters</span></span>
<span data-ttu-id="61fec-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fec-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61fec-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fec-139">입력</span><span class="sxs-lookup"><span data-stu-id="61fec-139">INPUTS</span></span>

### <span data-ttu-id="61fec-140">System.String</span><span class="sxs-lookup"><span data-stu-id="61fec-140">System.String</span></span>

## <span data-ttu-id="61fec-141">출력</span><span class="sxs-lookup"><span data-stu-id="61fec-141">OUTPUTS</span></span>

### <span data-ttu-id="61fec-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="61fec-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="61fec-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61fec-143">NOTES</span></span>

## <span data-ttu-id="61fec-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61fec-144">RELATED LINKS</span></span>
