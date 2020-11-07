---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 9fe8e36a752b4643ba44a59e8c44954bf25284c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702578"
---
# <span data-ttu-id="d5e79-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d5e79-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="d5e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5e79-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e79-103">지정 된 관리 되는 인스턴스에 대 한 투명 한 데이터 암호화 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5e79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5e79-104">SYNTAX</span></span>

```
Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5e79-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5e79-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e79-106">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate는 지정 된 관리 인스턴스에 대 한 투명 한 데이터 암호화 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-106">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="d5e79-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5e79-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e79-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5e79-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="d5e79-109">변수</span><span class="sxs-lookup"><span data-stu-id="d5e79-109">PARAMETERS</span></span>

### <span data-ttu-id="d5e79-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e79-110">-DefaultProfile</span></span>
<span data-ttu-id="d5e79-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5e79-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="d5e79-112">-ManagedInstanceName</span></span>
<span data-ttu-id="d5e79-113">관리 되는 인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="d5e79-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e79-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5e79-114">-PassThru</span></span>
<span data-ttu-id="d5e79-115">성공적으로 실행 되 면 추가 된 인증서 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="d5e79-116">-암호</span><span class="sxs-lookup"><span data-stu-id="d5e79-116">-Password</span></span>
<span data-ttu-id="d5e79-117">투명 한 데이터 암호화 인증서의 암호</span><span class="sxs-lookup"><span data-stu-id="d5e79-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e79-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="d5e79-118">-PrivateBlob</span></span>
<span data-ttu-id="d5e79-119">투명 한 데이터 암호화 인증서 용 개인 blob</span><span class="sxs-lookup"><span data-stu-id="d5e79-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e79-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e79-120">-ResourceGroupName</span></span>
<span data-ttu-id="d5e79-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d5e79-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e79-122">-확인</span><span class="sxs-lookup"><span data-stu-id="d5e79-122">-Confirm</span></span>
<span data-ttu-id="d5e79-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5e79-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5e79-124">-WhatIf</span></span>
<span data-ttu-id="d5e79-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5e79-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5e79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e79-127">CommonParameters</span></span>
<span data-ttu-id="d5e79-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e79-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e79-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e79-130">입력</span><span class="sxs-lookup"><span data-stu-id="d5e79-130">INPUTS</span></span>

### <span data-ttu-id="d5e79-131">않아야</span><span class="sxs-lookup"><span data-stu-id="d5e79-131">None</span></span>

## <span data-ttu-id="d5e79-132">출력</span><span class="sxs-lookup"><span data-stu-id="d5e79-132">OUTPUTS</span></span>

### <span data-ttu-id="d5e79-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d5e79-133">System.Boolean</span></span>

## <span data-ttu-id="d5e79-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d5e79-134">NOTES</span></span>

## <span data-ttu-id="d5e79-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5e79-135">RELATED LINKS</span></span>
