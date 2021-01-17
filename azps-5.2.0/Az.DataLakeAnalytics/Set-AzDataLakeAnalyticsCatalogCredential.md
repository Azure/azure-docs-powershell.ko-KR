---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345381"
---
# <span data-ttu-id="5c39d-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="5c39d-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="5c39d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c39d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c39d-103">Azure Data Lake Analytics 카탈로그 자격 증명 암호를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="5c39d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c39d-104">SYNTAX</span></span>

### <span data-ttu-id="5c39d-105">SetByHostNameAndPort(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c39d-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c39d-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="5c39d-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c39d-107">설명</span><span class="sxs-lookup"><span data-stu-id="5c39d-107">DESCRIPTION</span></span>
<span data-ttu-id="5c39d-108">이 Set-AzDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그와 연결된 자격 증명 암호를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="5c39d-109">예제</span><span class="sxs-lookup"><span data-stu-id="5c39d-109">EXAMPLES</span></span>

### <span data-ttu-id="5c39d-110">예제 1: 계정과 연결된 자격 증명의 암호 수정</span><span class="sxs-lookup"><span data-stu-id="5c39d-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="5c39d-111">이 명령은 자격 증명 암호를 NewPassword에 지정된 암호로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="5c39d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c39d-112">PARAMETERS</span></span>

### <span data-ttu-id="5c39d-113">-Account</span><span class="sxs-lookup"><span data-stu-id="5c39d-113">-Account</span></span>
<span data-ttu-id="5c39d-114">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5c39d-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="5c39d-115">-Credential</span></span>
<span data-ttu-id="5c39d-116">수정할 자격 증명의 이름 및 현재 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c39d-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5c39d-117">-CredentialName</span></span>
<span data-ttu-id="5c39d-118">수정할 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="5c39d-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="5c39d-119">-DatabaseHost</span></span>
<span data-ttu-id="5c39d-120">자격 증명이 연결할 수 있는 외부 데이터 원본의 호스트 이름을 mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="5c39d-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c39d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c39d-121">-DatabaseName</span></span>
<span data-ttu-id="5c39d-122">자격 증명을 보유하는 Data Lake Analytics 계정의 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="5c39d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c39d-123">-DefaultProfile</span></span>
<span data-ttu-id="5c39d-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c39d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c39d-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="5c39d-125">-NewPassword</span></span>
<span data-ttu-id="5c39d-126">자격 증명에 대한 새 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-126">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c39d-127">-Port</span><span class="sxs-lookup"><span data-stu-id="5c39d-127">-Port</span></span>
<span data-ttu-id="5c39d-128">이 자격 증명을 사용하여 지정된 DatabaseHost에 연결하는 데 사용되는 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c39d-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="5c39d-129">-Uri</span></span>
<span data-ttu-id="5c39d-130">이 자격 증명이 연결할 수 있는 외부 데이터 원본의 전체 URI(Uniform Resource Identifier)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c39d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c39d-131">-Confirm</span></span>
<span data-ttu-id="5c39d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c39d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c39d-133">-WhatIf</span></span>
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

### <span data-ttu-id="5c39d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c39d-134">CommonParameters</span></span>
<span data-ttu-id="5c39d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c39d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c39d-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5c39d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c39d-137">입력</span><span class="sxs-lookup"><span data-stu-id="5c39d-137">INPUTS</span></span>

### <span data-ttu-id="5c39d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5c39d-138">System.String</span></span>

### <span data-ttu-id="5c39d-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="5c39d-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5c39d-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="5c39d-140">System.Uri</span></span>

### <span data-ttu-id="5c39d-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5c39d-141">System.Int32</span></span>

## <span data-ttu-id="5c39d-142">출력</span><span class="sxs-lookup"><span data-stu-id="5c39d-142">OUTPUTS</span></span>

### <span data-ttu-id="5c39d-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="5c39d-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="5c39d-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c39d-144">NOTES</span></span>

## <span data-ttu-id="5c39d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c39d-145">RELATED LINKS</span></span>
