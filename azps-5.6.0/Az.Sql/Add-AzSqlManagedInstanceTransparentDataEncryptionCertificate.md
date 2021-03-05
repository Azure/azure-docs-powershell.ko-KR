---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 3a44d520e68fc1c2eec6593af728300a469760a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961499"
---
# <span data-ttu-id="36d95-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="36d95-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="36d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d95-102">SYNOPSIS</span></span>
<span data-ttu-id="36d95-103">주어진 관리되는 인스턴스에 대한 투명한 데이터 암호화 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="36d95-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="36d95-104">구문</span><span class="sxs-lookup"><span data-stu-id="36d95-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d95-105">설명</span><span class="sxs-lookup"><span data-stu-id="36d95-105">DESCRIPTION</span></span>
<span data-ttu-id="36d95-106">이 Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate 관리되는 인스턴스에 대한 투명한 데이터 암호화 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="36d95-107">예제</span><span class="sxs-lookup"><span data-stu-id="36d95-107">EXAMPLES</span></span>

### <span data-ttu-id="36d95-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="36d95-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="36d95-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="36d95-109">PARAMETERS</span></span>

### <span data-ttu-id="36d95-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d95-110">-DefaultProfile</span></span>
<span data-ttu-id="36d95-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d95-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="36d95-112">-ManagedInstanceName</span></span>
<span data-ttu-id="36d95-113">관리되는 인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="36d95-113">The managed instance name</span></span>

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

### <span data-ttu-id="36d95-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d95-114">-PassThru</span></span>
<span data-ttu-id="36d95-115">성공적인 실행에서 추가된 인증서 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="36d95-116">-Password</span><span class="sxs-lookup"><span data-stu-id="36d95-116">-Password</span></span>
<span data-ttu-id="36d95-117">투명한 데이터 암호화 인증서에 대한 암호</span><span class="sxs-lookup"><span data-stu-id="36d95-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="36d95-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="36d95-118">-PrivateBlob</span></span>
<span data-ttu-id="36d95-119">투명한 데이터 암호화 인증서에 대한 개인 Blob</span><span class="sxs-lookup"><span data-stu-id="36d95-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="36d95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d95-120">-ResourceGroupName</span></span>
<span data-ttu-id="36d95-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="36d95-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="36d95-122">-확인</span><span class="sxs-lookup"><span data-stu-id="36d95-122">-Confirm</span></span>
<span data-ttu-id="36d95-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d95-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d95-124">-WhatIf</span></span>
<span data-ttu-id="36d95-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d95-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d95-127">CommonParameters</span></span>
<span data-ttu-id="36d95-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36d95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d95-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36d95-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d95-130">입력</span><span class="sxs-lookup"><span data-stu-id="36d95-130">INPUTS</span></span>

### <span data-ttu-id="36d95-131">없음</span><span class="sxs-lookup"><span data-stu-id="36d95-131">None</span></span>

## <span data-ttu-id="36d95-132">출력</span><span class="sxs-lookup"><span data-stu-id="36d95-132">OUTPUTS</span></span>

### <span data-ttu-id="36d95-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36d95-133">System.Boolean</span></span>

## <span data-ttu-id="36d95-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36d95-134">NOTES</span></span>

## <span data-ttu-id="36d95-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36d95-135">RELATED LINKS</span></span>
