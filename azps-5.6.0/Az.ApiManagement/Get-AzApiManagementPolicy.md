---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dbabc98a8221cc2b870368b2b9cdd55e81280863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994611"
---
# <span data-ttu-id="f92d1-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f92d1-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="f92d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f92d1-103">지정된 범위 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="f92d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="f92d1-104">SYNTAX</span></span>

### <span data-ttu-id="f92d1-105">GetTenantLevel(기본값)</span><span class="sxs-lookup"><span data-stu-id="f92d1-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f92d1-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="f92d1-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f92d1-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="f92d1-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f92d1-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="f92d1-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f92d1-109">설명</span><span class="sxs-lookup"><span data-stu-id="f92d1-109">DESCRIPTION</span></span>
<span data-ttu-id="f92d1-110">**Get-AzApiManagementPolicy** cmdlet은 지정된 범위 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="f92d1-111">예제</span><span class="sxs-lookup"><span data-stu-id="f92d1-111">EXAMPLES</span></span>

### <span data-ttu-id="f92d1-112">예제 1: 테넌트 수준 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f92d1-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="f92d1-113">이 명령은 테넌트 수준 정책을 얻게 하여 테넌트 수준 정책을 tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="f92d1-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="f92d1-114">예제 2: 제품 범위 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f92d1-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="f92d1-115">이 명령은 제품 범위 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="f92d1-116">예제 3: API 범위 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f92d1-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="f92d1-117">이 명령은 API 범위 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="f92d1-118">예제 4: 작업 범위 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f92d1-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="f92d1-119">이 명령은 작업 범위 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="f92d1-120">예제 5: RawXml 형식으로 테넌트 범위 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f92d1-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="f92d1-121">이 명령은 Xml 이스케이프되지 않은 형식으로 테넌트 범위 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="f92d1-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f92d1-122">PARAMETERS</span></span>

### <span data-ttu-id="f92d1-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f92d1-123">-ApiId</span></span>
<span data-ttu-id="f92d1-124">기존 API의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="f92d1-125">이 매개 변수를 지정하면 cmdlet이 API 범위 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92d1-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f92d1-126">-ApiRevision</span></span>
<span data-ttu-id="f92d1-127">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-127">Identifier of API Revision.</span></span> <span data-ttu-id="f92d1-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-128">This parameter is optional.</span></span> <span data-ttu-id="f92d1-129">지정하지 않으면 현재 활성 API 개정에서 정책이 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92d1-130">-Context</span><span class="sxs-lookup"><span data-stu-id="f92d1-130">-Context</span></span>
<span data-ttu-id="f92d1-131">**PsApiManagementContext의 인스턴스를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f92d1-131">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f92d1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92d1-132">-DefaultProfile</span></span>
<span data-ttu-id="f92d1-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f92d1-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f92d1-134">-Force</span></span>
<span data-ttu-id="f92d1-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="f92d1-135">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92d1-136">-Format</span><span class="sxs-lookup"><span data-stu-id="f92d1-136">-Format</span></span>
<span data-ttu-id="f92d1-137">API 관리 정책의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="f92d1-138">이 매개 변수의 기본값은 "xml"입니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="f92d1-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f92d1-139">-OperationId</span></span>
<span data-ttu-id="f92d1-140">기존 API 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="f92d1-141">*ApiId를* 사용하여 이 매개 변수를 지정하는 경우 cmdlet은 작업 범위 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92d1-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f92d1-142">-ProductId</span></span>
<span data-ttu-id="f92d1-143">기존 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="f92d1-144">이 매개 변수를 지정하면 cmdlet이 제품 범위 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92d1-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="f92d1-145">-SaveAs</span></span>
<span data-ttu-id="f92d1-146">결과를 저장하기 위해 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="f92d1-147">이 매개 변수를 지정하지 않으면 결과는 스티로로 파이프라인됩니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="f92d1-148">-확인</span><span class="sxs-lookup"><span data-stu-id="f92d1-148">-Confirm</span></span>
<span data-ttu-id="f92d1-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f92d1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f92d1-150">-WhatIf</span></span>
<span data-ttu-id="f92d1-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f92d1-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f92d1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92d1-153">CommonParameters</span></span>
<span data-ttu-id="f92d1-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f92d1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92d1-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f92d1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92d1-156">입력</span><span class="sxs-lookup"><span data-stu-id="f92d1-156">INPUTS</span></span>

### <span data-ttu-id="f92d1-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f92d1-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f92d1-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f92d1-158">System.String</span></span>

### <span data-ttu-id="f92d1-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f92d1-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f92d1-160">출력</span><span class="sxs-lookup"><span data-stu-id="f92d1-160">OUTPUTS</span></span>

### <span data-ttu-id="f92d1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f92d1-161">System.String</span></span>

## <span data-ttu-id="f92d1-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f92d1-162">NOTES</span></span>

## <span data-ttu-id="f92d1-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f92d1-163">RELATED LINKS</span></span>

[<span data-ttu-id="f92d1-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f92d1-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="f92d1-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f92d1-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


