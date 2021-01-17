---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375558"
---
# <span data-ttu-id="6e62e-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6e62e-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="6e62e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e62e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e62e-103">주어진 관리되는 인스턴스에 대한 투명한 데이터 암호화 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="6e62e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e62e-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e62e-105">설명</span><span class="sxs-lookup"><span data-stu-id="6e62e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e62e-106">이 Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate 관리되는 인스턴스에 대해 투명한 데이터 암호화 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="6e62e-107">예제</span><span class="sxs-lookup"><span data-stu-id="6e62e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e62e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e62e-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="6e62e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e62e-109">PARAMETERS</span></span>

### <span data-ttu-id="6e62e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e62e-110">-DefaultProfile</span></span>
<span data-ttu-id="6e62e-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e62e-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="6e62e-112">-ManagedInstanceName</span></span>
<span data-ttu-id="6e62e-113">관리되는 인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="6e62e-113">The managed instance name</span></span>

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

### <span data-ttu-id="6e62e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e62e-114">-PassThru</span></span>
<span data-ttu-id="6e62e-115">성공한 실행 시 추가된 인증서 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="6e62e-116">-Password</span><span class="sxs-lookup"><span data-stu-id="6e62e-116">-Password</span></span>
<span data-ttu-id="6e62e-117">투명한 데이터 암호화 인증서에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="6e62e-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="6e62e-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="6e62e-118">-PrivateBlob</span></span>
<span data-ttu-id="6e62e-119">투명한 데이터 암호화 인증서에 대한 개인 Blob</span><span class="sxs-lookup"><span data-stu-id="6e62e-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="6e62e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e62e-120">-ResourceGroupName</span></span>
<span data-ttu-id="6e62e-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6e62e-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="6e62e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e62e-122">-Confirm</span></span>
<span data-ttu-id="6e62e-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e62e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e62e-124">-WhatIf</span></span>
<span data-ttu-id="6e62e-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6e62e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e62e-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e62e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e62e-127">CommonParameters</span></span>
<span data-ttu-id="6e62e-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e62e-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e62e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e62e-130">입력</span><span class="sxs-lookup"><span data-stu-id="6e62e-130">INPUTS</span></span>

### <span data-ttu-id="6e62e-131">없음</span><span class="sxs-lookup"><span data-stu-id="6e62e-131">None</span></span>

## <span data-ttu-id="6e62e-132">출력</span><span class="sxs-lookup"><span data-stu-id="6e62e-132">OUTPUTS</span></span>

### <span data-ttu-id="6e62e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e62e-133">System.Boolean</span></span>

## <span data-ttu-id="6e62e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e62e-134">NOTES</span></span>

## <span data-ttu-id="6e62e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e62e-135">RELATED LINKS</span></span>
