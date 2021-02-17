---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399501"
---
# <span data-ttu-id="2b377-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b377-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="2b377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b377-102">SYNOPSIS</span></span>
<span data-ttu-id="2b377-103">서버에서 위협 검색 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="2b377-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b377-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b377-105">설명</span><span class="sxs-lookup"><span data-stu-id="2b377-105">DESCRIPTION</span></span>
<span data-ttu-id="2b377-106">**Set-AzSqlServerThreatDetectionPolicy** cmdlet은 Azure SQL 서버에서 위협 검색 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="2b377-107">서버에서 위협 감지를 사용하도록 설정하려면 해당 서버에서 감사 정책을 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="2b377-108">이 cmdlet을 사용 하 고 서버를 식별 하는 *ResourceGroupName* 및 ServerName 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="2b377-109">예제</span><span class="sxs-lookup"><span data-stu-id="2b377-109">EXAMPLES</span></span>

### <span data-ttu-id="2b377-110">예제 1: 데이터베이스에 대한 위협 검색 정책 설정</span><span class="sxs-lookup"><span data-stu-id="2b377-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="2b377-111">이 명령은 Server01이라는 서버에 대한 위협 검색 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="2b377-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b377-112">PARAMETERS</span></span>

### <span data-ttu-id="2b377-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b377-113">-DefaultProfile</span></span>
<span data-ttu-id="2b377-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b377-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b377-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="2b377-115">-EmailAdmins</span></span>
<span data-ttu-id="2b377-116">위협 검색 정책이 전자 메일을 사용하여 관리자에게 연락하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="2b377-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="2b377-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="2b377-118">정책에서 제외할 검색 유형의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="2b377-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="2b377-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b377-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="2b377-120">Sql_Injection</span></span>
- <span data-ttu-id="2b377-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="2b377-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="2b377-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="2b377-122">Access_Anomaly</span></span>
- <span data-ttu-id="2b377-123">없음</span><span class="sxs-lookup"><span data-stu-id="2b377-123">None</span></span>

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

### <span data-ttu-id="2b377-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="2b377-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="2b377-125">정책에서 경고를 보내는 세미코론으로 구분된 전자 메일 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="2b377-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b377-126">-PassThru</span></span>
<span data-ttu-id="2b377-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b377-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b377-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b377-129">-ResourceGroupName</span></span>
<span data-ttu-id="2b377-130">서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="2b377-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2b377-131">-RetentionInDays</span></span>
<span data-ttu-id="2b377-132">감사 로그의 보존 기간(일)</span><span class="sxs-lookup"><span data-stu-id="2b377-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="2b377-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b377-133">-ServerName</span></span>
<span data-ttu-id="2b377-134">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2b377-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2b377-135">-StorageAccountName</span></span>
<span data-ttu-id="2b377-136">사용할 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="2b377-137">와일드카드는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-137">Wildcards are not permitted.</span></span> <span data-ttu-id="2b377-138">이 매개 변수는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-138">This parameter is not required.</span></span> <span data-ttu-id="2b377-139">이 매개 변수가 제공되지 않은 경우 cmdlet은 데이터베이스의 위협 검색 정책의 일부로 이전에 정의된 저장소 계정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="2b377-140">데이터베이스가 처음 정의되고 이 매개 변수가 제공되지 않은 경우 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="2b377-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b377-141">-Confirm</span></span>
<span data-ttu-id="2b377-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b377-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b377-143">-WhatIf</span></span>
<span data-ttu-id="2b377-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2b377-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b377-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b377-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b377-146">CommonParameters</span></span>
<span data-ttu-id="2b377-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b377-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b377-148">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b377-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b377-149">입력</span><span class="sxs-lookup"><span data-stu-id="2b377-149">INPUTS</span></span>

### <span data-ttu-id="2b377-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2b377-150">System.String</span></span>

### <span data-ttu-id="2b377-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b377-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2b377-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="2b377-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="2b377-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b377-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2b377-154">출력</span><span class="sxs-lookup"><span data-stu-id="2b377-154">OUTPUTS</span></span>

### <span data-ttu-id="2b377-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2b377-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="2b377-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b377-156">NOTES</span></span>

## <span data-ttu-id="2b377-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b377-157">RELATED LINKS</span></span>

[<span data-ttu-id="2b377-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2b377-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="2b377-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2b377-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
