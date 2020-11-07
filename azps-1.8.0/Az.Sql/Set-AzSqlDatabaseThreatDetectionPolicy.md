---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 231d38105851a5af7d32535d85827ce70e69caa5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698784"
---
# <span data-ttu-id="89f14-101">Set-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89f14-101">Set-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="89f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89f14-102">SYNOPSIS</span></span>
<span data-ttu-id="89f14-103">데이터베이스에 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-103">Sets a threat detection policy on a database.</span></span>

## <span data-ttu-id="89f14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89f14-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89f14-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89f14-105">DESCRIPTION</span></span>
<span data-ttu-id="89f14-106">**AzSqlDatabaseThreatDetectionPolicy** Cmdlet은 Azure SQL 데이터베이스에 대 한 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-106">The **Set-AzSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="89f14-107">데이터베이스에서 위협 검색을 사용 하도록 설정 하려면 해당 데이터베이스에서 감사 정책을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="89f14-108">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="89f14-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="89f14-110">예제의</span><span class="sxs-lookup"><span data-stu-id="89f14-110">EXAMPLES</span></span>

### <span data-ttu-id="89f14-111">예제 1: 데이터베이스에 대 한 위협 검색 정책 설정</span><span class="sxs-lookup"><span data-stu-id="89f14-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="89f14-112">이 명령은 Server01 라는 서버의 Database01 이라는 데이터베이스에 대 한 위협 검색 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="89f14-113">변수</span><span class="sxs-lookup"><span data-stu-id="89f14-113">PARAMETERS</span></span>

### <span data-ttu-id="89f14-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89f14-114">-DatabaseName</span></span>
<span data-ttu-id="89f14-115">정책이 설정 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="89f14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f14-116">-DefaultProfile</span></span>
<span data-ttu-id="89f14-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="89f14-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89f14-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="89f14-118">-EmailAdmins</span></span>
<span data-ttu-id="89f14-119">위협 검색 정책이 전자 메일을 사용 하 여 관리자에 게 보낼지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f14-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="89f14-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="89f14-121">정책에서 제외할 검색 유형의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="89f14-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89f14-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="89f14-123">Sql_Injection</span></span> 
- <span data-ttu-id="89f14-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="89f14-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="89f14-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="89f14-125">Access_Anomaly</span></span> 
- <span data-ttu-id="89f14-126">않아야</span><span class="sxs-lookup"><span data-stu-id="89f14-126">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f14-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="89f14-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="89f14-128">정책에서 알림을 보내는 전자 메일 주소 목록 (세미콜론으로 구분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f14-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89f14-129">-PassThru</span></span>
<span data-ttu-id="89f14-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89f14-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89f14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89f14-132">-ResourceGroupName</span></span>
<span data-ttu-id="89f14-133">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="89f14-134">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="89f14-134">-RetentionInDays</span></span>
<span data-ttu-id="89f14-135">감사 로그 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="89f14-135">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f14-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89f14-136">-ServerName</span></span>
<span data-ttu-id="89f14-137">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="89f14-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89f14-138">-StorageAccountName</span></span>
<span data-ttu-id="89f14-139">사용할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="89f14-140">와일드 카드는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-140">Wildcards are not permitted.</span></span> <span data-ttu-id="89f14-141">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-141">This parameter is not required.</span></span> <span data-ttu-id="89f14-142">이 매개 변수를 제공 하지 않으면 cmdlet에서 이전에 정의한 저장소 계정을 데이터베이스의 위협 검색 정책의 일부로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="89f14-143">데이터베이스 위협 검색 정책을 처음 정의 하는 경우이 매개 변수를 제공 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f14-144">-확인</span><span class="sxs-lookup"><span data-stu-id="89f14-144">-Confirm</span></span>
<span data-ttu-id="89f14-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89f14-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89f14-146">-WhatIf</span></span>
<span data-ttu-id="89f14-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89f14-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89f14-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f14-149">CommonParameters</span></span>
<span data-ttu-id="89f14-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89f14-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f14-151">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89f14-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f14-152">입력</span><span class="sxs-lookup"><span data-stu-id="89f14-152">INPUTS</span></span>

### <span data-ttu-id="89f14-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89f14-153">System.String</span></span>

### <span data-ttu-id="89f14-154">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89f14-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="89f14-155">ThreatDetection. DetectionType []/. \*</span><span class="sxs-lookup"><span data-stu-id="89f14-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="89f14-156">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89f14-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="89f14-157">출력</span><span class="sxs-lookup"><span data-stu-id="89f14-157">OUTPUTS</span></span>

### <span data-ttu-id="89f14-158">ThreatDetection. DatabaseThreatDetectionPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="89f14-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="89f14-159">상속자</span><span class="sxs-lookup"><span data-stu-id="89f14-159">NOTES</span></span>

## <span data-ttu-id="89f14-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89f14-160">RELATED LINKS</span></span>

[<span data-ttu-id="89f14-161">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89f14-161">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="89f14-162">제거-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="89f14-162">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="89f14-163">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="89f14-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


