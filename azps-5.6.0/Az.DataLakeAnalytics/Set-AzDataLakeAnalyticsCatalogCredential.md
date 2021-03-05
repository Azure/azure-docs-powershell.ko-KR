---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 51af3aeffe5cf75835507e78b4638270b255fb29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988246"
---
# <span data-ttu-id="fbcdf-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="fbcdf-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="fbcdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbcdf-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcdf-103">Azure Data Lake Analytics 카탈로그 자격 증명 암호를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="fbcdf-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbcdf-104">SYNTAX</span></span>

### <span data-ttu-id="fbcdf-105">SetByHostNameAndPort(기본값)</span><span class="sxs-lookup"><span data-stu-id="fbcdf-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbcdf-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="fbcdf-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcdf-107">설명</span><span class="sxs-lookup"><span data-stu-id="fbcdf-107">DESCRIPTION</span></span>
<span data-ttu-id="fbcdf-108">Set-AzDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그와 연결된 자격 증명 암호를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="fbcdf-109">예제</span><span class="sxs-lookup"><span data-stu-id="fbcdf-109">EXAMPLES</span></span>

### <span data-ttu-id="fbcdf-110">예제 1: 계정과 연결된 자격 증명의 암호 수정</span><span class="sxs-lookup"><span data-stu-id="fbcdf-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="fbcdf-111">이 명령은 NewPassword에 지정된 암호로 자격 증명 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="fbcdf-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fbcdf-112">PARAMETERS</span></span>

### <span data-ttu-id="fbcdf-113">-Account</span><span class="sxs-lookup"><span data-stu-id="fbcdf-113">-Account</span></span>
<span data-ttu-id="fbcdf-114">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fbcdf-115">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="fbcdf-115">-Credential</span></span>
<span data-ttu-id="fbcdf-116">수정할 자격 증명의 이름 및 현재 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="fbcdf-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fbcdf-117">-CredentialName</span></span>
<span data-ttu-id="fbcdf-118">수정할 자격 증명의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="fbcdf-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="fbcdf-119">-DatabaseHost</span></span>
<span data-ttu-id="fbcdf-120">자격 증명이 연결할 수 있는 외부 데이터 원본의 호스트 이름을 mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="fbcdf-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbcdf-121">-DatabaseName</span></span>
<span data-ttu-id="fbcdf-122">자격 증명을 보유한 Data Lake Analytics 계정의 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="fbcdf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcdf-123">-DefaultProfile</span></span>
<span data-ttu-id="fbcdf-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fbcdf-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbcdf-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="fbcdf-125">-NewPassword</span></span>
<span data-ttu-id="fbcdf-126">자격 증명에 대한 새 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="fbcdf-127">-Port</span><span class="sxs-lookup"><span data-stu-id="fbcdf-127">-Port</span></span>
<span data-ttu-id="fbcdf-128">이 자격 증명을 사용하여 지정된 DatabaseHost에 연결하는 데 사용되는 포트 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="fbcdf-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="fbcdf-129">-Uri</span></span>
<span data-ttu-id="fbcdf-130">이 자격 증명이 연결할 수 있는 외부 데이터 원본의 전체 URI(균일한 리소스 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="fbcdf-131">-확인</span><span class="sxs-lookup"><span data-stu-id="fbcdf-131">-Confirm</span></span>
<span data-ttu-id="fbcdf-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbcdf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbcdf-133">-WhatIf</span></span>
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

### <span data-ttu-id="fbcdf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcdf-134">CommonParameters</span></span>
<span data-ttu-id="fbcdf-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcdf-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fbcdf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcdf-137">입력</span><span class="sxs-lookup"><span data-stu-id="fbcdf-137">INPUTS</span></span>

### <span data-ttu-id="fbcdf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fbcdf-138">System.String</span></span>

### <span data-ttu-id="fbcdf-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="fbcdf-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="fbcdf-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="fbcdf-140">System.Uri</span></span>

### <span data-ttu-id="fbcdf-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fbcdf-141">System.Int32</span></span>

## <span data-ttu-id="fbcdf-142">출력</span><span class="sxs-lookup"><span data-stu-id="fbcdf-142">OUTPUTS</span></span>

### <span data-ttu-id="fbcdf-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="fbcdf-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="fbcdf-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbcdf-144">NOTES</span></span>

## <span data-ttu-id="fbcdf-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbcdf-145">RELATED LINKS</span></span>
