---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 7e08c66798c76fe6e03fb26602b7895f49d12322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532044"
---
# <span data-ttu-id="ccedf-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="ccedf-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="ccedf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccedf-102">SYNOPSIS</span></span>
<span data-ttu-id="ccedf-103">Azure Data Lake Analytics 카탈로그 자격 증명 암호를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccedf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccedf-104">SYNTAX</span></span>

### <span data-ttu-id="ccedf-105">SetByHostNameAndPort (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccedf-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccedf-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="ccedf-106">SetByFullURI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccedf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ccedf-107">DESCRIPTION</span></span>
<span data-ttu-id="ccedf-108">Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그와 연결 된 자격 증명 암호를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="ccedf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ccedf-109">EXAMPLES</span></span>

### <span data-ttu-id="ccedf-110">예제 1: 계정에 연결 된 자격 증명 암호 수정</span><span class="sxs-lookup"><span data-stu-id="ccedf-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="ccedf-111">이 명령은 NewPassword에 지정 된 암호로 자격 증명 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="ccedf-112">변수</span><span class="sxs-lookup"><span data-stu-id="ccedf-112">PARAMETERS</span></span>

### <span data-ttu-id="ccedf-113">-계정</span><span class="sxs-lookup"><span data-stu-id="ccedf-113">-Account</span></span>
<span data-ttu-id="ccedf-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ccedf-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="ccedf-115">-Credential</span></span>
<span data-ttu-id="ccedf-116">수정할 자격 증명의 이름과 현재 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="ccedf-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ccedf-117">-CredentialName</span></span>
<span data-ttu-id="ccedf-118">수정할 자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="ccedf-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="ccedf-119">-DatabaseHost</span></span>
<span data-ttu-id="ccedf-120">자격 증명을 mydatabase.contoso.com 형식으로 연결할 수 있는 외부 데이터 원본의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="ccedf-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccedf-121">-DatabaseName</span></span>
<span data-ttu-id="ccedf-122">자격 증명을 보유 하 고 있는 Data Lake Analytics 계정에서 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="ccedf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccedf-123">-DefaultProfile</span></span>
<span data-ttu-id="ccedf-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ccedf-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccedf-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="ccedf-125">-NewPassword</span></span>
<span data-ttu-id="ccedf-126">자격 증명의 새 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="ccedf-127">-포트</span><span class="sxs-lookup"><span data-stu-id="ccedf-127">-Port</span></span>
<span data-ttu-id="ccedf-128">이 자격 증명을 사용 하 여 지정 된 DatabaseHost에 연결 하는 데 사용 되는 포트 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="ccedf-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="ccedf-129">-Uri</span></span>
<span data-ttu-id="ccedf-130">이 자격 증명이 연결할 수 있는 외부 데이터 원본의 전체 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="ccedf-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ccedf-131">-Confirm</span></span>
<span data-ttu-id="ccedf-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccedf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccedf-133">-WhatIf</span></span>
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

### <span data-ttu-id="ccedf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccedf-134">CommonParameters</span></span>
<span data-ttu-id="ccedf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccedf-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccedf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccedf-137">입력</span><span class="sxs-lookup"><span data-stu-id="ccedf-137">INPUTS</span></span>

### <span data-ttu-id="ccedf-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ccedf-138">System.String</span></span>

### <span data-ttu-id="ccedf-139">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ccedf-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ccedf-140">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="ccedf-140">System.Uri</span></span>

### <span data-ttu-id="ccedf-141">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ccedf-141">System.Int32</span></span>

## <span data-ttu-id="ccedf-142">출력</span><span class="sxs-lookup"><span data-stu-id="ccedf-142">OUTPUTS</span></span>

### <span data-ttu-id="ccedf-143">DataLake. USqlCredential-. \*</span><span class="sxs-lookup"><span data-stu-id="ccedf-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="ccedf-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ccedf-144">NOTES</span></span>

## <span data-ttu-id="ccedf-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccedf-145">RELATED LINKS</span></span>
